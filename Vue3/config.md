## vue3 config



#### getCurrentInstance 的使用（不推荐使用）

```vue

//  - main.js

const app = createApp(App);

app.config.globalProperties.$userInfo = {
    name:'xxxx',
		age:'19',
		eat(){
			console.log('eat food!!')
		}
}
app.mount('#app')


// App.vue

<template>
	<div>
    {{$userInfo.name}} // 'xxxx'
  </div>
</template>

import {getCurrentInstance} from 'vue';

setup(){
// 用proxy appContext打包之后会有问题 且 ts中没有提示
	const {proxy} = getCurrentInstance() as ComponentInternalInstance;
	proxy.$userInfo // {name:'xxxx',age:'19',...}

//
	const {appContext} = getCurrentInstance();
    appContext.config.globalProperties.$userInfo //{name:'xxxx',age:'19'.......}
}
```

tips：https://v3.cn.vuejs.org/api/composition-api.html#provide-inject



### isCustomElement

```js
-vite 中配置
plugins: [
    vue({
      reactivityTransform: true,
      template: {
     		compilerOptions: {
      		isCustomElement: (tag) => tag.startsWith('jsjs-')
        }
    	}
    }),
      

-vue-Cli中
  chainWebpack: config => {
     config.module
       .rule('vue')
       .use('vue-loader')
       .tap(options => {
         options.compilerOptions = {
           ...(options.compilerOptions || {}),
           isCustomElement: tag => /^(jsjsjs)-/i.test(tag)
         };
         return options;
       })
   }

```

