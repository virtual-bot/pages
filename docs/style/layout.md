# Flex布局

Voltron 的样式排版使用了 Flex 布局。值得注意的是，尚不兼容网页的百分比布局。

---

<!-- toc -->

# display

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/display)

`display`属性可以设置元素的内部和外部显示类型 display types，默认值为flex。

| 类型                                                            | 必需 | 默认值 |
| --------------------------------------------------------------- | -------- | -----|
| enum('flex', 'none') | 否 | flex |

注：如果实际使用时发现`display: none`有异常问题，建议使用`v-if`先进行规避

# flexDirection

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/flex-direction)

`flexDirection` 决定了容器的子元素的排列方向：`row` 代表水平排列, `column` 代表垂直排列。其他两个参数是反向排列。
它跟 css 的 flex-direction 定义很像，但 css 是默认值为 `row`，而 Voltron 默认是 `column`。

| 类型                                                   | 必需 | 默认值 |
| ------------------------------------------------------ | -------- | ------- |
| enum('row', 'row-reverse', 'column', 'column-reverse') | 否       | column |

# flexWrap

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/flex-wrap)

`flexWrap` 定义了子元素如何在接触到父容器底部时执行换行的行为。

| 类型                   | 必需 | 默认值 | 
| ---------------------- | -------- | ------ |
| enum('wrap', 'nowrap', 'wrap-reverse) | 否  | nowrap |

# alignItems

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/align-items)

`alignItems`决定了子元素在次轴方向的排列方式（此样式设置在父元素上）。例如若子元素本来是沿着竖直方向排列的（即主轴竖直，次轴水平），则`alignItems`决定了它们在水平方向的排列方式。此样式和CSS中的`alignItems`表现一致，默认值为stretch。

| 类型                                                            | 必需 | 默认值 |
| --------------------------------------------------------------- | -------- | -----|
| enum('flex-start', 'flex-end', 'center', 'stretch', 'baseline') | 否       | flex-start |

# alignSelf

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/align-self)

`alignSelf`决定了元素在父元素的次轴方向的排列方式（此样式设置在子元素上），其值会覆盖父元素的`alignItems`的值。其表现和 CSS 上的`align-self`一致（默认值为auto）。

| 类型                                                                    | 必需 | 默认值 |
| ----------------------------------------------------------------------- | -------- | ------ |
| enum('auto', 'flex-start', 'flex-end', 'center', 'stretch', 'baseline') | 否       | auto (优先级遵循父级align-items) |

# justifyContent

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/justify-content)

`justifyContent` 定义了浏览器如何分配顺着父容器主轴的弹性元素之间及其周围的空间。

| 类型                                                                                      | 必需 | 默认值 |
| ----------------------------------------------------------------------------------------- | -------- | ------ |
| enum('flex-start', 'flex-end', 'center', 'space-between', 'space-around', 'space-evenly') | 否       | flex-start |

# flex

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/flex)

在 Voltron 中 flex 的表现和 CSS 有些区别。 flex 在 Voltron 中只能为整数值。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# flexGrow

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/flex-grow)

`flexGrow` 定义伸缩项目的扩展能力。它接受一个不带单位的值做为一个比例。主要用来决定伸缩容器剩余空间按比例应扩展多少空间。

如果所有伸缩项目的 `flex-grow` 设置了 `1`，那么每个伸缩项目将设置为一个大小相等的剩余空间。如果你给其中一个伸缩项目设置了 `flex-grow` 值为 `2`，那么这个伸缩项目所占的剩余空间是其他伸缩项目所占剩余空间的两倍。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# flexShrink

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/flex-shrink )

`flexShrink` 属性指定了 flex 元素的收缩规则。flex 元素仅在默认宽度之和大于容器的时候才会发生收缩，其收缩的大小是依据 flex-shrink 的值。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# flexBasis

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/flex-basis)

`flex-basis` 指定了 flex 元素在主轴方向上的初始大小。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |