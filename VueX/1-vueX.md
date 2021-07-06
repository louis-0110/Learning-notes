## vueX是什么

就是一个响应式的变量存储器

```js
Vue.prototype.store = {
  name:'xiaoming'
}

this.store.name

类似于这种，但是vueX是能做到响应式于所有的组件中
```

## vueX管理什么状态呢？

1. 用户的登录状态token、用户名称、头像、地理位置信息等等
2. 商品的收藏、购物车中的物品等等

