# 盒子模型

盒子模型就把html页面中的布局元素看作是一个矩形的盒子，也就是一个盛装内容的容器。

---

<!-- toc -->

# boxSizing

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing)

`boxSizig` 属性定义了计算一个元素的总宽度和总高度。

| 类型                                                            | 必需 | 默认值 |
| --------------------------------------------------------------- | -----| -----|
| enum('border-box') | 否 | border-box |

# width

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/width)

`width`定义了容器的宽度

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# maxWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/max-width)

与css中`max-width`类似，定义了容器最大的宽度

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# minWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/min-width)

与css中`min-width`类似，定义了容器最小的宽度

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# height

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/height)

`height` 定义了容器的高度

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# maxHeight

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/max-height)

与css中`max-height`类似，定义了容器最大的高度

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# minHeight

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/min-height)

与css中`min-height`类似，定义了容器最小的高度

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# margin

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/margin)

设置 `margin` 与同时对`marginTop`, `marginLeft`, `marginBottom`, 和 `marginRight`设置了同样的值效果一致。

注：`margin`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须使用`marginTop`, `marginLeft`, `marginBottom`, 和 `marginRight`

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# marginTop

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/margin-top)

`marginTop` 和 CSS 的 `margin-top` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# marginRight

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/margin-right)

`marginRight` 与 CSS 的 `margin-right` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |



# marginBottom

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/margin-bottom)

`marginBottom` 和 CSS 的 `margin-bottom` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# marginLeft

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/margin-left)

`marginLeft` 与 CSS 的 `margin-left` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# padding

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/padding)

设置 `padding` 与同时设置`paddingTop`, `paddingBottom`, `paddingLeft`, 和 `paddingRight`一个值时效果一致。

注：`padding`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须使用`paddingTop`, `paddingBottom`, `paddingLeft`, 和 `paddingRight`

| 类型            | 必需 |
| --------------- | -------- |
| numbe | 否       |

# paddingTop

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/padding-top)

`paddingTop` 和 CSS 的 `padding-top` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# paddingRight

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/padding-right)

`paddingRight` 和 CSS 的 `padding-right` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# paddingBottom

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/padding-bottom)

`paddingBottom` 与 CSS 的 `padding-bottom` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# paddingLeft

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/padding-left)

`paddingLeft` 与 CSS 的 `padding-left` 类似。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# border

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border)

`border`是一个用于设置各种单独的边界属性的简写属性。

注：`border`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`方向`和`属性`，如`borderTopWidth`, `borderRightColor`

| 类型   | 必需 | 备注 |
| ------ | -------- | ----- |
| enum('number 边框类型 颜色') | 否       | 必须三个值全写 |

# borderTop

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-top)

`borderTop`是属性`borderTopColor`,`borderTopStyle`, 和`borderTopWidth`三者的缩写。

注：`borderTop`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderTopColor`,`borderTopStyle`, 和`borderTopWidth`

| 类型   | 必需 | 备注 |
| ------ | -------- | ----- |
| enum('number 边框类型 颜色') | 否       | 必须三个值全写 |


# borderRight

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-right)

`borderRight`是属性`borderRightColor`, `borderRightStyle`, 和`borderRightWidth`三者的缩写。

注：`borderRight`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderRightColor`, `borderRightStyle`, 和`borderRightWidth`

| 类型   | 必需 | 备注 |
| ------ | -------- | ----- |
| enum('number 边框类型 颜色') | 否       | 必须三个值全写 |


# borderBottom

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-bottom)

`borderBottom`是属性`borderBottomColor`, `borderBottomStyle`, 和`borderBottomWidth`三者的缩写。

注：`borderBottom`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderBottomColor`, `borderBottomStyle`, 和`borderBottomWidth`

| 类型   | 必需 | 备注 |
| ------ | -------- | ----- |
| enum('number 边框类型 颜色') | 否       | 必须三个值全写 |

# borderLeft

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-left)

`borderLeft`是属性`borderLeftColor`, `borderLeftStyle`, 和`borderLeftWidth`的三者的缩写。

注：`borderLeft`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderLeftColor`, `borderLeftStyle`, 和`borderLeftWidth`

| 类型   | 必需 | 备注 |
| ------ | -------- | ----- |
| enum('number 边框类型 颜色') | 否       | 必须三个值全写 |

# borderWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-width)

`borderWidth`和CSS上的`border-width`表现类似，是`borderTopWidth`, `borderRightWidth`, `borderBottomWidth`和`borderLeftWidth`的缩写。

注：`borderWidth`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderTopWidth`, `borderRightWidth`, `borderBottomWidth`和`borderLeftWidth`

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderTopWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-top-width)

`borderTopWidth`和 CSS 上的`border-top-width`表现一致。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderRightWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-right-width)

`borderRightWidth` 和 CSS 上的`border-right-width`表现一致。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderBottomWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-bottom-width)

`borderBottomWidth`和 CSS 上的`border-bottom-width`表现一致。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderLeftWidth

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/border-left-width)

`borderLeftWidth`和 CSS 上的`border-left-width`表现一致。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderColor

注：`borderColor`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderTopColor`, `borderRightColor`, `borderBottomColor`和`borderLeftColor`

| 类型               | 必需 |
| ------------------ | -------- |
| [color](css-unit.md) | 否       |

# borderTopColor

| 类型               | 必需 |
| ------------------ | -------- |
| [color](css-unit.md) | 否       |

# borderRightColor

| 类型               | 必需 |
| ------------------ | -------- |
| [color](css-unit.md) | 否       |

# borderBottomColor

| 类型               | 必需 |
| ------------------ | -------- |
| [color](css-unit.md) | 否       |

# borderLeftColor

| 类型               | 必需 |
| ------------------ | -------- |
| [color](css-unit.md) | 否       |

# borderStyle

注：`borderStyle`属性合并书写只在`<style></style>`标签中提供支持，如果使用内联样式，则必须指明`borderTopStyle`, `borderRightStyle`, `borderBottomStyle`和`borderLeftStyle`

| 类型                              | 必需 |
| --------------------------------- | -------- |
| enum('solid', 'dotted', 'dashed') | 否       |

# borderTopStyle

| 类型                              | 必需 |
| --------------------------------- | -------- |
| enum('solid', 'dotted', 'dashed') | 否       |

# borderRightStyle

| 类型                              | 必需 |
| --------------------------------- | -------- |
| enum('solid', 'dotted', 'dashed') | 否       |

# borderBottomStyle

| 类型                              | 必需 |
| --------------------------------- | -------- |
| enum('solid', 'dotted', 'dashed') | 否       |

# borderLeftStyle

| 类型                              | 必需 |
| --------------------------------- | -------- |
| enum('solid', 'dotted', 'dashed') | 否       |

# borderRadius

| 类型   | 必需 | 默认值 |
| ------ | -------- | ------ |
| number | 否       |   0   |

# borderTopRightRadius

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderBottomRightRadius

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderTopLeftRadius

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# borderBottomLeftRadius

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |

# overflow

`overflow` 定义了子元素超过父容器宽高度后的显示情况 `overflow: hidden` 的情况会导致子元素被父容器切割超出显示范围的部分 `overflow: visible` 会让子容器正常显示全部，即使超出父容器的显示范围。

| 类型                                | 必需 | 默认值 |
| ----------------------------------- | -------- | ----- |
| enum('visible', 'hidden') | 否       | hodden |






