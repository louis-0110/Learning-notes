## ref='domEle'

```vue
<template>
	<div ref='oDiv'>
    xxx
  </div>

	<ul>
    <li v-for'(item,index) of list' ref='el=> {if(el) listDom[index] = el}'></li>
  </ul>
</template>

<script>
	export default{
    name:'test',
    
    setup(){
      const oDiv = ref(null);
      const listDom = ref([]);
      
      return {
        oDiv,
        listDom
      }
    }
  }
</script>
```



