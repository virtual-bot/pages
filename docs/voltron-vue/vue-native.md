<!-- markdownlint-disable no-duplicate-header -->

# 终端能力

voltron-vue 通过在 Vue 上绑定了一个 `Native` 属性，实现获取终端设备信息、以及调用终端能力。也可以用来监测是否在 Voltron 环境下运行。

> [[范例：native.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/global-module/native.vue)

# 获取设备信息

它无需任何方法，直接取值即可。

## version

获取 voltron-vue 的版本，注意，非终端SDK版本

示例

```javascript
console.log(Vue.Native.version);
```

## Device

获取设备名称，iPhone 可以拿到具体的 iPhone 型号，Android 设备暂时只能拿到 `Android device`的文本。

示例

```javascript
console.log(Vue.Native.Device);
```


<!-- ## OSVersion

iOS 版本。 -->

## APILevel

Android 操作系统版本。

示例

```javascript
console.log(Vue.Native.APILevel); // 30
```

<!-- ## SDKVersion

Voltron 终端 SDK 版本。 -->

## Platform

获取操作系统，ios 或 android

示例

```javascript
console.log(Vue.Native.Platform); // android or ios
```

## Dimensions

获取屏幕分辨率。

示例

```javascript
const { window, screen } = Vue.Native.Dimensions;
console.log(`屏幕尺寸：${screen.height}x${screen.width}`);
console.log(`带状态栏的窗口尺寸：${window.height}x${window.width}`);
console.log(`状态栏高度：${screen.statusBarHeight}`)
```

## PixelRatio

获取设备像素比例。

## 示例

```javascript
console.log(Vue.Native.PixelRatio); // 3
```

## isIPhoneX

获取是否是异形屏幕的 iPhoneX

## 示例

```javascript
console.log(Vue.Native.isIPhoneX); // 3
```

## screenIsVertical

屏幕是否横屏过来了

## 示例

```javascript
console.log(Vue.Native.screenIsVertical); // 3
```

## OnePixel

一个像素的 dp/pt 值。

## 示例

```javascript
console.log(Vue.Native.OnePixel); // 3
```

# 调用终端能力

## callNative/callNativeWithPromise

调用终端模块的方法，`callNative` 一般用于无返回的模块方法调用，callNativeWithPromise 一般用于有返回的模块方法调用，它会返回一个带着结果的 Promise。

## measureInWindow

测量窗口可视范围内某个组件的尺寸和位置，如果出错会都是 -1。

