<!-- markdownlint-disable no-duplicate-header -->

# 核心组件

核心组件的定义是跟浏览器、Vue 中保持一致，如果只使用这些组件的话，可以直接跨浏览器。

# a

一切同 [p](voltron-vue/components.md?id=p)。

# button

一切同[div](voltron-vue/components.md?id=div)

# div

[[范例：component-div.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-div.vue)

## 子元素

支持所有元素，包括`div`

## 样式

支持除文字样式外所有样式（需要注意，这里文字样式与web端不同，不存在继承关系，所以不能给元素加文字样式以控制其子元素表现）

注：需要额外特殊说明的是，div元素默认内部不可滚动。但是可以通过增加样式参数 `overflow-y: scroll` 切换为可以纵向滚动容器，或者增加样式参数 `overflow-x: scroll` 切换为水平滚动容器，这里`overflow-y`和`overflow-x`不可当做样式来看待，实质上是将`div`转化为终端的`ScrollView`组件，所以`overflow-y`或`overflow-x`在这里是可以和`overflow`共存的。

## 属性

无

## 事件

[通用事件](voltron-vue/gesture.md)

支持`click`, `longClick`, `pressIn`, `pressOut`, `touchStart`, `touchMove`, `touchend`, `touchCancel`

独有事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| layout           | 这个事件会在布局计算完成后立即调用一次，可能存在多次调用。 | `Function`                           | `ALL`     |

## 方法

### scrollTo

> **注意：** (只有`overflow-x: scroll`或`overflow-y: scroll`为`true`时可用)

`(xOffset: number, yOffset: number: duration: number) => void` 通知 ScrollView 滑动到某个具体坐标偏移值(offset)的位置。

参数：

> * `xOffset`: number - 滑动到 X 方向的 offset，`overflow-x: scroll`可用
> * `yOffset`: number - 滑动到 Y 方向的 offset，`overflow-y: scroll`可用
> * `number`: boolean - 多长事件滚到指定位置

返回：void

# form

一切同[div](voltron-vue/components.md?id=div)

# img

## 子元素

不支持

## 样式

支持除文字样式外所有样式

[[范例：component-img.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-img.vue)

图片组件，和浏览器的一样。

> **注意：** 图片容器宽高如果为0，图片不会自动撑开，布局时一定要保证宽高有效。

## 属性

| 参数          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| src        | 图片地址，支持本地资源，远程资源 | string                                | `ALL`    |
| defaultSource | 默认占位图片，必须填写使用`data:image/png;base64`类型 | string | `ALL`    |
| resizeMode | 图片适配方式 | enum('contain', 'cover', 'center', 'stretch', 'repeat') | `ALL` |
| capInsets | 点九图参数设置，例：{top: 45,left: 25,right: 80,bottom: 25} | Object | `ALL` |

## 事件

[通用事件](voltron-vue/gesture.md)

支持`click`, `longClick`, `pressIn`, `pressOut`

独有事件：

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| layout      | 当元素挂载或者布局改变的时候调用，参数为： `{ nativeEvent: { layout: { x, y, width, height } } }`。 | `Function`                                                   | `ALL`    |
| load        | 加载成功完成时调用此回调函数。                               | `Function`                                                   | `ALL`    |
| loadStart   | 加载开始时调用。 | `Function`                                                   | `ALL`    |
| loadEnd     | 加载结束后，不论成功还是失败，调用此回调函数。               | `Function`                                                   | `ALL`    |
| error       | 当加载错误的时候调用此回调函数。| `Function`                                                   | `ALL`    |

## 方法

无

# input

[[component-input.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-input.vue)

单行文本组件。

## 子元素

不支持

## 样式

支持所有样式（包括文字样式）

## 属性

| 参数                  | 描述                                                         | 类型                                                         | 支持平台  |
| --------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------- |
| defaultValue          | 提供一个文本框中的初始值。当用户开始输入的时候，值就可以改变。  在一些简单的使用情形下，如果你不想用监听消息然后更新 value 属性的方法来保持属性和状态同步的时候，就可以用 defaultValue 来代替。 | `string`                                                     | `ALL`     |
| disabled              | 如果为 true                           | `boolean`                                                    | `ALL`     |
| type          | 决定弹出的何种软键盘的。 注意，`password`仅在属性 `multiline=false` 单行文本框时生效。 | `enum`(default, numeric, password, email, phone-pad) | `ALL`     |
| maxlength             | 限制文本框中最多的字符数。 | `numbers`                                                    | `ALL`     |
| numberOfLines         | 设置 `input` 的最大行数，在使用的时候必需同时设置 `multiline` 参数为 `true`。 | `number`                                                     | `ALL`     |
| multiline         | 设置多行时必须开启 | `boolean`                                                  | `ALL`     |
| placeholder           | 如果没有任何文字输入，会显示此字符串。                       | `string`                                                     | `ALL`     |
| placeholderTextColor  | 占位字符串显示的文字颜色。                                   | [`color`](style/color.md)                                | `ALL`     |
| returnKeyType         | 指定软键盘的回车键显示的样式。                               | `enum`(done, go, next, search, send)              | `ALL`     |
| value                 | 指定 `input` 组件的值。                                  | `string`                                                     | `ALL`     |
| caretColor | 指定光标颜色 | [`color`](style/color.md) | `ALL` |

## 事件

[通用事件](voltron-vue/gesture.md)

不支持

独有事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| focus                | 当文本框获得焦点的时候调用此回调函数。                       | `Function`                                                   | `ALL`     |
| blur                | 当文本框失去焦点的时候调用此回调函数。                       | `Function`                                                   | `ALL`     |
| input                | 输入监听                       | `Function`                                                   | `ALL`     |
| chang          | 当文本框内容变化时调用此回调函数。改变后的文字内容会作为参数传递。 | `Function`                                                   | `ALL`     |
| endEditing          | 当文本输入结束后调用此回调函数。可用来监听用户点击键盘完成键                             | `Function`                                                   | `ALL`     |
| layout              | 当组件挂载或者布局变化的时候调用，参数为`{ x, y, width, height }`。 | `Function`                                                   | `ALL`     |
| select     | 当输入框选择文字的范围被改变时调用。返回参数的样式如 `{ nativeEvent: { selection: { start, end } } }`。需要注意，输入时该方法也会调用，每输入一个文字，其实选中区域都会前进一步，所以这里实际使用时最好判断一下`start`和`end`是否相等 | `Function`                                                   | `ALL`     |

## 方法

### focus

主动获得焦点（异步）：`this.$refs.refName.focus();`

参数：无

返回：void

### blur

主动失焦（异步）： `this.$refs.refName.blur();`

参数：无

返回：void

### blur

主动清空文本（异步） `this.$refs.refName.clear();`

参数：无

返回：void

### setValue

设置文本内容（异步） `this.$refs.refName.setValue(text);`

参数：

> * `text`: String - 文本内容

返回：void

### getValue

获取当前文本内容（异步）

参数：无

返回：`Promise<string>`


# label

显示文本。

一切同 [p](voltron-vue/components.md?id=p)。

# li

ul 的子节点，终端层节点回收和复用的最小颗粒度。

[[范例：component-list.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-list.vue)

## 子元素

支持任意子元素

## 参数

| 参数                  | 描述                                                         | 类型                                                        | 支持平台 |
| --------------------- | ------------------------------------------------------------ | ----------------------------------------------------------- | -------- |
| key             | 指定一个函数，在其中返回对应条目的 Key 值，详见 [Vue 官文](//cn.vuejs.org/v2/guide/list.html) | `(index: number) => any`                                    | `ALL`    |
| sticky       | 对应的item是否需要使用悬停效果（滚动到顶部时，会悬停在List顶部，不会滚出屏幕） | `boolean`                                | `ALL`    |

# p

[[范例：component-p.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-p.vue)

显示文本，不过因为 Voltron 下没有 `display: inline` 的显示模式，默认全部都是 flex 的。

## 子元素

支持文字标签`p`，`span`，`label`，`a`

## 属性

| 参数          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| numberOfLines | 行数限制，超出后的行为需要在css中的text-overflow进行限制 | `number`                                  | `ALL`    |

## 事件

[通用事件](voltron-vue/gesture.md)

支持`click`, `longClick`, `pressIn`, `pressOut`

通用事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| layout           | 这个事件会在布局计算完成后立即调用一次，不过收到此事件时新的布局可能还没有在屏幕上呈现，尤其是一个布局动画正在进行中的时候。 | `Function`                           | `ALL`     |

## 方法

无

# ul

[[范例：component-list.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-list.vue)

## 子元素

只支持`li`

## 参数

| 参数                  | 描述                                                         | 类型                                                        | 支持平台 |
| --------------------- | ------------------------------------------------------------ | ----------------------------------------------------------- | -------- |
| initialContentOffset  | 初始位移值 -- 在列表初始化时即可指定滚动距离，避免初始化后再通过 scrollTo 系列方法产生的闪动。 | `number`                                                    | `ALL`
| scrollEventThrottle   | 指定滑动事件的回调频率，传入数值指定了多少毫秒(ms)组件会调用一次 `onScroll` 回调事件，默认 200ms | `number`                                                    | `ALL`    |
| showScrollIndicator   | 是否显示垂直滚动条。  | `boolean`                                                   | `ALL`    |
| rowShouldSticky   | 是否有固定元素  | `boolean`                                                   | `ALL`    |

## 事件

[通用事件](voltron-vue/gesture.md)

支持`click`, `longClick`, `pressIn`, `pressOut`

独有事件

| 事件名称          | 描述                                                         | 类型                                      | 支持平台 |
| ------------- | ------------------------------------------------------------ | ----------------------------------------- | -------- |
| endReached          | 当所有的数据都已经渲染过，并且列表被滚动到最后一条时，将触发 `onEndReached` 回调。 | `Function`                                                  | `ALL`    |
| momentumScrollBegin | 在 `ScrollView` 开始滑动的时候调起                           | `Function`                                                  | `ALL`    |
| momentumScrollEnd   | 在 `ScrollView` 结束滑动的时候调起                           | `Function`                                                  | `ALL`    |
 scroll              | 当触发 `ListView` 的滑动事件时回调，在 `ListView` 滑动时回调，因此调用会非常频繁，请使用 `scrollEventThrottle` 进行频率控制。 注意：ListView 在滚动时会进行组件回收，不要在滚动时对 renderRow() 生成的 ListItemView 做任何 ref 节点级的操作（例如：所有 callUIFunction 和 measureInWindow 方法），回收后的节点将无法再进行操作而报错。 | `(obj: { contentOffset: { x: number, y: number } }) => any` | `ALL`    |
| scrollBeginDrag     | 当用户开始拖拽 `ScrollView` 时调用。                         | `Function`                                                  | `ALL`    |
| scrollEndDrag       | 当用户停止拖拽 `ScrollView` 或者放手让 `ScrollView` 开始滑动的时候调用 | `Function`                                                  | `ALL`    |

## 方法

### scrollTo

`(xOffset: number, yOffset: number: duration: number) => void` 通知 ListView 滑动到某个具体坐标偏移值(offset)的位置。

> * `xOffset`: 0
> * `yOffset`: numbere - 滑动到 Y 方向的 offset
> * `number`: boolean - 多长事件滚到指定位置

### scrollToIndex

`(xIndex: number, yIndex: number: animated: boolean) => void` 通知 ListView 滑动到第几个 item。

> * `xIndex`: number - 0
> * `yIndex`: numbere - 滑动到 Y 方向的 xIndex 个 item
> * `animated`: boolean - 滑动过程是否使用动画


# span

一切同 [p](voltron-vue/components.md?id=p)。

# textarea

一切同 [input](voltron-vue/components.md?id=input)。

[[范例：component-textarea.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/basic-component/component-textarea.vue)

这里唯一的区别是`textarea`组件默认`multiline`为`true`
