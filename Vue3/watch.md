## watch



```js
const count = reg(0);
const state = reactive({count:0})

//监听state.count
watch(()=> state.count,(newV,oldV)=>{
	console.log('数据改变了！')
})

//监听count
watch(count,(newV,oldV)=>{
	console.log('count 改变了！')
})

//一次监听多个值
watch([count,()=>state.count], ([newV1,newV2],[oldV1,oldV2])=>{
	console.log('数据改变了！')
})
```



1. 当数据改改变时才会执行

