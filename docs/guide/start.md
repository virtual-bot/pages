# 开始接入

> **`注意`** 目前机器人开发暂时仅支持`vue`语法，`react`支持将在后续推出。

机器人开发方案是Vue的子集，整体开发体验类似RN，Weex等动态化方案。

# 进入开发

1. `git clone https://github.com/virtual-bot/webpack-vue-demo`

    首先我们拉取demo项目

2. `cd webpack-vue-demo && npm install`

    进入项目后安装`npm`依赖

3. 进入`src/main-native.js`修改`appName`为自己的BOT名称，如果不修改，会导致后续页面白屏。

    ```javascript
    const app = new Vue({
        // 这里要写上自己的BOT名称
        appName: 'Demo',
        // 根节点，必须是 Id，当根节点挂载时才会触发上屏
        rootView: '#root',
        // 渲染自己
        render: h => h(App),
    });
    ```

4. `npm run voltron:dev`

    启动webpack进行构建

5. 通过usb链接安卓手机（暂不支持ios设备调试），执行`npm run voltron:debug`

    该步骤实质上做了两件事
    1. 在本地构建产物目录下启动网络服务，端口为`38989`。
    2. 通过`adb reverse tcp:38989 tcp:38989`，将电脑端的`38989`端口映射到安卓系统。

    如果你看到`adb: error: no devices/emulators found`的字样，证明安卓设备链接电脑并未识别，建议检查设备链接情况。如果看到端口号输出，则无误。

6. 启动APP，点击群组右上角`...`->`群BOT管理`->`选择自己要开发的机器人`->`弹窗右上角设置`->`功能设置 debug mode`

    通过上面链路，理论上这个时候就能够打开一个BOT的页面，如果你看到的是白屏，需要注意`appName`是否有修改为自己的BOT，另外需要说明的是，`功能设置 debug mode`固定为链接本地的调试服务，`功能设置`则是线上使用的版本，另外当我们修改前端页面后，也可以通过调试页上的绿色按钮进行快速重新刷新，（live reload功能正在计划中）。

7. 开始愉快的进行开发吧~

# 框架指引

接下来，为了辅助你的开发，我们还准备了几个模块

1. [如何调试](guide/debug.md)
2. [框架能力介绍](voltron-vue/introduction.md)
3. [样式支持介绍](style/css-unit.md)

# 常见问题

1. 作为开发者，我如何知道用户的权限信息，例如用户是否能够修改机器人配置

    在框架的`created`生命周期中，我们植入了三个变量
    ```javascript
    created () {
        const params = getApp()?.$options?.$superProps?.params ?? {};
        this.gid = params.gid;
        this.botId = params.botId;
        this.sig = params.sig;
    }
    ```
    通过`sig`参数在后台可换取有限的用户信息。