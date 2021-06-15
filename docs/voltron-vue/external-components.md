<!-- markdownlint-disable no-duplicate-header -->

# 终端扩展组件

# dialog

[[范例：component-dialog.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/extend-component/component-dialog.vue)

> **注意：** 使用时必须用v-if控制显示

## 子元素

内部第一层元素必须用`<div>`包裹，且设置为绝对定位全屏

## 样式支持

不支持任何样式，内部div包裹的元素可支持所有样式

## 参数

| 参数          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| animated              | 弹出时是否需要带动画                                                            | `boolean`                                                    | `ALL`    |
| animationType         | 动画效果                                                            | `enum`(none, slide, fade, pop, slide_fade, slide-top, slide-right, slide-left) | `ALL`    |
| animationDuration         | 动画时间(ms)                                                          | `number`  | `ALL`    |
| barrierColor         | 默认背景为透明，动画效果是渐变出来                                                        | [`color`](style/color.md)  | `ALL`    |
| immersionStatusBar    | 是否是沉浸式状态栏。                                         | `boolean`                                                    | `ALL`    |
| darkStatusBarText     | 是否是亮色主体文字，默认字体是黑色的，改成 true 后会认为 Modal 背景为暗色调，字体就会改成白色。 | `boolean`                                                    | `ALL`    |

## 事件

## 事件

[通用事件](./gesture.md)

不支持

独有事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| show                | 在`Modal`显示时会执行此回调函数。                            | `Function`                                                   | `ALL`    |
| requestClose        | 在`Modal`请求关闭时会执行此回调函数，一般时在 Android 系统里按下硬件返回按钮时触发，一般要在里面处理关闭弹窗。 | `Function`                                                   | `Android`    |

# swiper

[[范例：component-swiper.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/extend-component/component-swiper.vue)

轮播组件，里面只能包含 `<swiper-slide>` 组件。

> **注意事项：**如果在 ul 里嵌套 swiper，因为 ul 自带复用能力，swiper 滚出屏幕后不可在对其进行任何操作（例如通过代码更改 current 值），否则很可能导致终端出错。

## 子组件

只支持[`swiper-slide`](#swiper-slide)

## 样式

支持所有样式（包括文字样式）

## 属性

| 参数                     | 描述                                                         | 类型                                         | 支持平台 |
| ------------------------ | ------------------------------------------------------------ | -------------------------------------------- | -------- |
| current              | 实时改变当前所处页码 | `number`                                     | `ALL`    |
| initialPage              | 指定一个数字，用于决定初始化后默认显示的页面index，默认不指定的时候是0 | `number`                                     | `ALL`    |
| scrollEnabled            | 指定ViewPager是否可以滑动，默认为true                        | `boolean`                                    | `ALL`    |

## 事件

[通用事件](./gesture.md)

不支持

独有事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| dragging                | 拖动时触发。                            | `Function`                                                   | `ALL`    |
| dropped   | 拖拽松手时触发，就是确定了滚动的页面时触发。                                                            | `Function`                                                   | `ALL`    |
| stateChanged*   | 手指行为发生改变时触发，包含了 idle、dragging、settling 三种状态，通过 state 参数返回                                                             | `Function`                                                   | `ALL`    |

* stateChanged 三种值的意思：
  * idle 空闲状态
  * dragging 拖拽中
  * settling 松手后触发，然后马上回到 idle

## 方法

### setSlide

滑动到index：`this.$refs.refName.setSlide(slideIndex);`

参数：
> * `slideIndex`: number - 页码

返回：void

### setSlideWithoutAnimation

滑动到index（无动画）：`this.$refs.refName.setSlideWithoutAnimation(slideIndex);`

参数：
> * `slideIndex`: number - 页码

返回：void


# swiper-slide

[[范例：component-swiper.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/extend-component/component-swiper.vue)

轮播组件页容器。

## 子组件

支持任意组件

## 样式

支持所有样式

## 属性

无

## 事件

[通用事件](./gesture.md)

支持`click`, `longClick`, `pressIn`, `pressOut`

独有事件

无

## 方法

无

# ul-refresh-wrapper

[[范例：component-swiper.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/extend-component/component-list-refresh.vue)

列表下拉刷新组件

## 子组件

支持`<ul-refresh>` 和 `<ul>` 

## 样式

支持除文字样式外所有样式

## 属性

无

## 事件

[通用事件](./gesture.md)

无

独有事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| refresh                | 下拉刷新回弹后触发刷新回掉函数的事件。*                            | `Function`                                                   | `ALL`    |

* 刷新事件回调的特别说明，刷新完成后，记得手动调用`refreshCompleted`结束刷新。

## 方法

### refreshCompleted

告知终端内容刷新已经结束，收起刷新栏。：`this.$refs.refName.refreshCompleted();`

### startRefresh

手动告知终端开始刷新，下拉刷新栏。：`this.$refs.refName.startRefresh();`

# ul-refresh

[[范例：demo-list-refresh.vue]](//github.com/Tencent/Voltron/blob/master/examples/voltron-vue-demo/src/components/native-demos/demo-list-refresh.vue)

列表下拉刷新时，刷新内容的容器组件。

## 子组件

支持任意组件

## 样式

支持除文字样式外所有样式

## 属性

无

## 事件

无

## 方法

无
