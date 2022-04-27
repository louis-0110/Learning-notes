### 在组件中使用

```js
{
	data(){
    return {}
	},
  filters: {
  	capitalize(value) {
    	if (!value) return ''
   	 	value = value.toString()
    	return value.charAt(0).toUpperCase() + value.slice(1)
  	}
	}
}
```



### 在全局定义

```js
Vue.filter('capitalize', function (value) {
  if (!value) return ''
  value = value.toString()
  return value.charAt(0).toUpperCase() + value.slice(1)
})

//初始化vue
new Vue({
  // ...
})
```

```vue

<div>{{ pie4 | capitalize('yi','er')}}</div> // pie4--yi--er

{
  data(){
    return{
    pie4= 'pie4'
    }
  },
	filters:{
    capitalize(value,v1,v2){
      return value+'--'+v1+'--'+v2
    }
  },
}
```

