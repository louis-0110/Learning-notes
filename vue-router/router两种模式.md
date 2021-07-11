## hash

```js
location.hash = 'foo';
```

> 用`location.hash`改变hash值，用onhashchange 监听 hash 变化

## history

```js
history.pushState({},'','home');
history.pushState({},'','about');
history.repalceState({},'','infomation')
history.back();
history.forward()
history.go()
```

> 用 `history.pushState` 改变`url` ,在内部用方法 实现页面的更新，用`popstate` 事件监听浏览器 前进 后退事件
>
> tips: `popstate` 无法监听 `history.pushState` 和 `history.repalceState`事件

原理：https://www.jianshu.com/p/557f2ba86892

