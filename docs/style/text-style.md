# 文字样式

关于设置文字样式的相关属性。

---

<!-- toc -->

# color

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/color_value)

* `'red'`
* `'#f0f'` (#rgb)
* `'#ff00ff'` (#rrggbb)
* `'rgb(255, 0, 255)'`
* `'rgba(255, 255, 255, 1.0)'`

# font-size

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/font-size)

font-size属性指定字体的大小。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| number | 否 |

# font-style

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/font-style)

font-style属性定义字体的风格。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('normal', 'italic') | 否 |

# font-weight

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/font-weight)

font-weight属性指定了字体的粗细程度。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('normal', 'bold', '100~900') | 否 |

# text-decoration

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/text-decoration)

text-decoration属性是用于设置文本的修饰线外观的（下划线、上划线、贯穿线/删除线）它是 text-decoration-line, text-decoration-color, text-decoration-style属性的缩写。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('none', 'underline', 'line-through') | 否 |

# text-align

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/text-align)

text-align属性定义行内内容（例如文字）如何相对它的块父元素对齐。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('left', 'right', 'center') | 否 |

# font-family

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/font-family)

font-family允许您通过给定一个有先后顺序的，由字体名或者字体族名组成的列表来为选定的元素设置字体。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('字体名称') | 否 |

# text-overflow

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/text-overflow)

text-overflow属性确定如何向用户发出未显示的溢出内容信号，在使用标签内配上属性numberOfLines，类型number。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('clip', 'ellipsis', 'fade') | 否 |

# white-space

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/white-space)

white-space属性是用来设置如何处理元素中的空白。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| enum('normal', 'pre', 'pre-line') | 否 |

# line-height

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/line-height)

line-height属性用于设置多行元素的空间量，如多行文本的间距。

注：line-height暂时只支持px，不支持1，1.5，2类似的字好倍数写法。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| number | 否 |

