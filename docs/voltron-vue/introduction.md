
# voltron-vue 介绍

voltron-vue 其实是基于官方 Vue 2.x 源代码，通过改写 [node-ops](//github.com/Tencent/Voltron/blob/master/packages/voltron-vue/src/runtime/node-ops.js) 外挂实现的自定义渲染层，但不仅仅是个到终端的渲染层，还同时实现前端组件到终端的映射、CSS 语法解析，和其它跨端框架不同，它尽力将 Web 端的开发体验带到终端上来，同时保持了对 Web 生态的兼容。