## vue3.0 路由配置

安装

```she
npm i vue-router@4
```

配置路由

```js
import {createRouter,createWebHistory} from 'vue-router';

const router = createRouter({
  history:createWebHistory(), // hash模式  base放在createWebHistory('/dist/')
	routes:[]
})
```

