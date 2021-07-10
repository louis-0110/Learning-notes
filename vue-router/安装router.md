### 安装 Router

```js
npm i vue-router
```

### 创建路由文件

-src

 -router

​	-index.js

​	-routes.js

---

--indexjs

```js
import Vue from 'vue';
import VueRouter from 'vue-router';
import routes from './routes'
Vue.use(VueRouter);

export default new VueRouter({
  routes,
  mode:'history'
})
```

-- routes.js

```js
const routes = [
  {
    name:'',
    path:'',
    component:()=> import()
  },
  {
    name:'',
    path:'',
    component:()=> import()
  }
]

export default routes;
```

