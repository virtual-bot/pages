# 前端调试

# 安卓调试方法

按照[进入开发](guide/start.md)的步骤开始后，打开`chrome://inspect`，首先确保 `Discover USB devices` 的复选框呈未选中状态，然后确保 `Discover network targets` 选中，并在右侧 `Configure` 按钮的弹窗中包含了 `localhost:38989` 调试服务地址，下方的 `Remote Target` 中应该会出现 `Voltron debug` 字样，点击下方的 `inspect` 链接即可打开 Chrome 调试器。

![Chrome inspect](//puui.qpic.cn/vupload/0/1577798490075_9tezu60gzzo.png/0)

![Chrome inspect button](../image/voltron_inspector_btn.png)

Voltron现阶段提供以下几个调试功能
# Element

在Element的Tab中，可以对页面元素进行查看，编辑等操作
![Chrome inspect button](../image/voltron_inspector_element.png)

# Network

在Network的Tab中，可以查看当前页面的网络请求
![Chrome inspect button](../image/voltron_inspector_network.png)

# Console

在Console的Tab中，可以直接查看console信息

# 断点调试

在项目中输入`debugger;`，重新运行即可
