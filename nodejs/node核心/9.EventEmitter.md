## EventEmitter

事件通用管理机制

```js
const {EventEmitter} = require('events');

//创建一个事件处理对象
const ee = new EventEmitter();

// 注册事件
ee.on('abc',()=>{
  console.log('abc事件触发了')
})

const fn1 = ()=>{
  console.log('abc事件触发了')
}
ee.on('abc',fn1)

// 触发一次
ee.once('bcd',()=>{
	console.log('这个事件只会触发一次')
})

// 触发事件
ee.emit('abc')
ee.emit('bcd')

// 注销事件
ee.off('abc',fn1)
```

