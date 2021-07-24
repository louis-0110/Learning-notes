### keep-alive

Vue 内置组件 用于缓冲组件

使用后会有两个生命周期

1. beforeDestroy 销毁前
2. destroyed 销毁后



- `include` - 字符串或正则表达式。只有名称匹配的组件会被缓存。
- `exclude` - 字符串或正则表达式。任何名称匹配的组件都不会被缓存。
- `max` - 数字。最多可以缓存多少组件实例。

