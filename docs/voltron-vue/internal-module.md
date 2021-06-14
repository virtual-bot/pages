<!-- markdownlint-disable no-duplicate-header -->

# 内置模块

[[范例：module.vue]](https://github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/global-module/module.vue)

# Cookie

Voltron 中通过 fetch 服务返回的 `set-cookie` Header 会自动将 Cookie 保存起来，下次再发出请求的时候就会带上，然后终端提供了这个界面让 业务可以获取或者修改保存好的 Cookie。

## getAll(url)

| 参数 | 类型     | 必需 | 参数意义 |
| --------  | -------- | -------- |  -------- |
| url | string | 是       | 获取指定 URL 下设置的 cookie |

返回值：

* `Prmoise<string>`，类似 `name=someone;gender=female` 的字符串，需要业务自己手工解析一下。

## set(url, keyValue, expireDate)

参数：

| 参数 | 类型     | 必需 | 参数意义 |
| -------- | -------- | -------- |  -------- |
| url | string | 是       | 设置指定 URL 下设置的 cookie |
| keyValue | string | 是       | 需要设置成 Cookie 的完整字符串，例如`name=someone;gender=female` |
| expreDate | Date | 否 | Date 类型的过期时间，不填不过期 |

# Clipboard

剪贴板读写模块，但是目前只支持纯文本。

## getString()

返回值：

* string

## setString(content)

| 参数 | 类型     | 必需 | 参数意义 |
| --------  | -------- | -------- |  -------- |
| content | string | 是       | 保存进入剪贴板的内容 |

# 事件监听

`getApp().$on()`: 时间监听

`getApp().$emit()` 事件触发

# 路由

建议用`dialog`代替

# localStorage

> 异步方法，需要在方法前面前面加上 `await`。

## 方法

### localStorage.getItem

`(key: string) => Promise<string>` 根据 key 值获取对应数据。

> * key: string - 需要获取值的目标 key


### localStorage.removeItem

`(key: string) => void` 根据 key 值删除对应数据。

> * key: string - 需要删除的目标 key

### localStorage.setItem

`(key: string, value: string) => void` 根据 key 和 value 设置保存键值对。

> * key: string - 需要获取值的目标 key
> * value: string - 需要获取值的目标值

# fetch

Voltron 提供了跟 W3C 标准基本一致的 [fetch](//developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API) 方法，可以直接参考 [MDN](//developer.mozilla.org/zh-CN/docs/Web/API/Fetch_API)。

> 注意：`fetch` 目前仅支持 JSON 对象的传输，别的格式暂时无法支持。

## 发起请求

如果需要请求远程地址，只需要在 fetch 函数参数值传入地址即可，如下：

```javascript
fetch('//mywebsite.com/mydata.json');
```

fetch 函数也支持 HTTP 请求的配置。

```javascript
fetch('//mywebsite.com/endpoint/', {
  method: 'POST',
  headers: {
    Accept: 'application/json',
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    firstParam: 'yourValue',
    secondParam: 'yourOtherValue',
  }),
});
```

完整的 fetch 请求属性列表可以[点击此处查看](//developer.mozilla.org/zh-CN/docs/Web/API/Request)。

## 处理返回值

返回数据将以 [Promise](//developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise) 的形式返回，示例如下：

```javascript
function getMoviesFromApi() {
  return fetch('//mywebsite.com/demo.json')
    .then(rsp => rsp.json())
    .then(json => json.movies)
    .catch(error => console.error(error));
}
```

可以使用 [async/await](//developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/async_function) 处理 fetch 返回的数据。

> 在使用 `fetch` 发起网络请求的时候，需要记得捕获错误，否则错误会被静默丢弃。

```javascript
async function getMoviesFromApi() {
  try {
    const rsp = await fetch('//mywebsite.com/demo.json');
    const json = await rsp.json();
    return responseJson.movies;
  } catch (error) {
    console.error(error);
  }
}
```

# WebSocket

[[范例：websocket.vue]](//github.com/virtual-bot/webpack-vue-demo/blob/master/src/components/global-module/websocket.vue)

# 定时器

[定时器](//developer.mozilla.org/en-US/Add-ons/Code_snippets/Timers)在 Javascript 中有非常广泛的应用，在 Voltron 也提供了支持。

Voltron 端定时器用法与 Web 端 Javascript 用法一致，可以直接使用。

## 方法

* [setTimeout](//developer.mozilla.org/zh-CN/docs/Web/API/Window/setTimeout)
* [clearTimeout](//developer.mozilla.org/zh-CN/docs/Web/API/WindowTimers/clearTimeout)
* [setInterval](//developer.mozilla.org/zh-CN/docs/Web/API/Window/setInterval)
* [clearInterval](//developer.mozilla.org/zh-CN/docs/Web/API/window/clearInterval)
