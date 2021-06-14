# background

关于background简写下的相关背景属性。

---

<!-- toc -->

# background-color

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-color)

background-color会设置元素的背景色

* `'red'`
* `'#f0f'` (#rgb)
* `'#ff00ff'` (#rrggbb)
* `'rgb(255, 0, 255)'`
* `'rgba(255, 255, 255, 1.0)'`

# background-image

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-image)

background-image属性用于为一个元素设置一个或者多个背景图像。

* `'url(http://xxxxx)'`(远程路径)
* `'url(../../assets)'`(相对路径)
* `'linear-gradient(to right, #000, #fff)'`(线性渐变)demo
    ```css
    background-image: linear-gradient(#e66465, #9198e5);
    background-image: linear-gradient(45deg, red, blue);
    background-image: linear-gradient(135deg, orange 60%, cyan);
    background-image: linear-gradient(to right, red 20%, orange 20% 40%, yellow 40% 60%, green 60% 80%, blue 80%);
    ```
    

# background-size

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-size)

background-size设置背景图片大小。图片可以保有其原有的尺寸，或者拉伸到新的尺寸，或者在保持其原有比例的同时缩放到元素的可用空间的尺寸。

* `'cover'`
* `'contain'`
* `'auto'`
* `'fit'` 该属性暂时替代web端中的`100% 100%`

# background-repeat

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-repeat)

background-repeat属性定义背景图像的重复方式。

* `'no-repeat'`
* `'repeat'`
* `'repeat-x'`
* `'repeat-y'`

# background-position

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-position)

background-position为每一个背景图片设置初始位置。

* `'center'`
* `'left center'`
* `'center bottom'`

注：暂不支持数字及百分比

# background-position-x

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-position-x)

background-position-x属性设置水平方向的位置。

| 类型                                                            | 必需 | 默认值 |
| --------------------------------------------------------------- | -------- | ------ |
| enum('left', 'center', 'right') | 否 | left |

# background-position-y

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/background-position-y)

background-position-y属性设置垂直方向上的位置。

| 类型                                                            | 必需 | 默认值 |
| --------------------------------------------------------------- | -------- | ----- |
| enum('top', 'center', 'bottom') | 否 | top |

# box-shadow

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow)

box-shadow 属性用于在元素的框架上添加阴影效果。

demo
```css
/* x偏移量 | y偏移量 | 阴影模糊半径 | 阴影扩散半径 | 阴影颜色 */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);
/* x偏移量 | y偏移量 | 阴影模糊半径 | 阴影颜色 */
box-shadow: 10px 5px 5px black;
/* 任意数量的阴影，以逗号分隔 */
box-shadow: 3px 3px red, -3px 0 2px olive;
```

注：暂不支持内阴影

# opacity

[[MDN 文档]](//developer.mozilla.org/zh-CN/docs/Web/CSS/opacity)

opacity属性指定了一个元素的不透明度。

| 类型                                                            | 必需 |
| --------------------------------------------------------------- | -------- |
| number | 否 |
