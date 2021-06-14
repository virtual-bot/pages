# 定位

定位允许您从正常的文档流布局中取出元素，并使它们具有不同的行为，例如放在另一个元素的上面，或者始终保持在浏览器视窗内的同一位置

---

<!-- toc -->

# position

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/position)

`position` 在 Voltron 里表现与 CSS基本一致, 但是所有时候都是默认为 `relative`, 所以当元素设置 `absolute` 的时候可以保证永远只对上一级父元素绝对定位。

它和 CSS 的'position'属性类似，但voltron内的`position`只有`absolute`与`relative`两个属性。

注：由于原生页面默认全屏布局，所以要实现`fixed`样式，只需要将页面可滚动元素包裹一层即可，如果需要`sticky`布局，则可以参考ListView（ul）中的固定属性

| 类型                         | 必需 | 默认值 |
| ---------------------------- | -------- | ------ |
| enum('absolute', 'relative') | 否       | relative |

# top

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/top)

`top` 值是指将本组件定位到距离顶部多少个逻辑像素（顶部的定义取决于position属性）。

它的表现和 CSS 上的top类似，但注意在React Native上只能使用逻辑像素值（数字单位），而不能使用百分比、em或是任何其他单位。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# right

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/right)

`right` 值是指将本组件定位到距离右边多少个逻辑像素（右边的定义取决于position属性）。

它的表现和 CSS 上的right类似，但注意在React Native上只能使用逻辑像素值（数字单位），而不能使用百分比、em或是任何其他单位。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# bottom

[MDN 文档](//developer.mozilla.org/zh-CN/docs/Web/CSS/bottom)

`bottom` 值是指将本组件定位到距离底部多少个逻辑像素（底部的定义取决于position属性）。

它的表现和 CSS 上的bottom类似，但注意在Voltron上只能使用逻辑像素值（数字单位），而不能使用百分比、em、rem、vh 或是任何其他单位。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# left

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/left)

`left` 值是指将本组件定位到距离左边多少个逻辑像素（左边的定义取决于position属性）。

它的表现和 CSS 上的 left 类似，但注意在 Voltron 上只能使用逻辑像素值（数字单位），而不能使用百分比、em或是任何其他单位。

| 类型            | 必需 |
| --------------- | -------- |
| number | 否       |

# zIndex

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/z-index)

`zIndex` 决定了容器排列的顺序。一般情况下，你无需直接使用 `zIndex`，容器元素会按照节点树的顺序依次渲染，在后面的元素会覆盖前面的元素（如果有覆盖情况的话）。`zIndex` 可以在你需要手动指定绘制层级的情况使用。

| 类型   | 必需 |
| ------ | -------- |
| number | 否       |
