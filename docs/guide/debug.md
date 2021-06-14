# 前端调试

# 安卓调试方法

1. `git clone https://github.com/virtual-bot/webpack-vue-demo`
2. `npm install`
3. `npm run voltron:dev`
4. 链接手机，`npm run voltron:debug`，启动调试服务
5. 启动Voltron-Vue-Demo，点击本地调试中的进入调试按钮
6. 然后打开 [Chrome](//www.google.com/chrome/)，输入 `chrome://inspect`，首先确保 `Discover USB devices` 的复选框呈未选中状态，然后确保 `Discover network targets` 选中，并在右侧 `Configure` 按钮的弹窗中包含了 `localhost:38989` 调试服务地址，下方的 `Remote Target` 中应该会出现 `Voltron debug tools for V8` 字样，点击下方的 `inspect` 链接即可打开 Chrome 调试器。

    ![Chrome inspect](//puui.qpic.cn/vupload/0/1577798490075_9tezu60gzzo.png/0)

7. 点击界面上的刷新按钮可触发终端刷新。
