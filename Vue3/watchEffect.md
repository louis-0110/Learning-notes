## watchEffect

1. 首次立即执行
2. 或在生命周期onMounted之前调用
3. 依赖改变的时候自动执行
4. 组件卸载的时候会停止侦听
5. readonly的值在里面是可读的
6. 会返回一个stop的函数，用于停止侦听
7. 可以传入onInvalidate函数用与处理有副作用的异步代码。

```js

const stop = watchEffect(async (onInvalidata)=>{
  const data = await getData();
  onInvalidata(()=>{
    console.log('onInvalidata is triggered')
  })
})

// 0 
// onInvalidata is ...
// 1 
// onInvalidata is ...
// 2
```

8. 默认会在onBeforUpdate之前调用，可以用{flush:'post'} 设置成之后调用

9. 开启开发模式下的debugger

```js
{
  onTrack(){ //开始就执行一次，数据变化执行
  	debugger;
},
  onTrigger(){ //数据变化才会执行
    debugger;
  }
}
```

