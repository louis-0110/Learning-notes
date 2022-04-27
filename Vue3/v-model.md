## 数据双向绑定 v-model

```vue
<!-- vue2 -->
<ChildComponent :value = 'pageTitle' @input='pageTitle = $event' />
<!-- 简写 -->
<ChildComponent v-model='pageTitle' />


<!-- vue3 -->
<ChildComponent
  :modelValue='pageTitle'
  @update:modelValue='pageTitle = $event'
/>

<!-- 简写为 -->
<ChildComponent v-model='pageTitle' />
```

多个双向绑定

```vue
<!-- vue2 -->
<ChildComponent v-model='pageTitle' :text.sync='someText'/>

<!-- vue3  简写为-->
<ChildComponent v-model='pageTitle' v-model:text='someText'/>
```





```vue

<template>
<div>
  <input type='checkbox' :value='someValue' @input='handleChange'/>
  <input type='text':value='someValue' v-on:[eventType]='handleChange2'/>
 <!-- <input :modelValue='someValue' @update:modelValue='someValue = $event'/>	-->
</div>
</template>


<script>
	export default{
    name:'childComponent',
    emits:['update:modelValue','update:title'],
  	 setup(props,{emit,attrs,slots,expose}){
     const handleChange1 = (e)=>{
         		emit('update:modelValue',e.target.value);
       		}
     const handleChange2 = (e)=>{
       			emit('update:title',e.target.value)
     			} 
       
    }
  }
</script>
```



```vue
<childComponent v-model='xxxx' />
```

