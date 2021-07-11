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
  mode:'history',
  linkActiveClass:'active'  // 修改按钮活跃的类名
})
```

-- routes.js

```js
const routes = [
  {
    path:'/',
    redirect:'/home' // 重定向
  },
  {
    name:'home',
    path:'/home',
    component:()=> import('@/views/home'),
    children:[
      {
      	path:'/',
        redirect:'news'
  	  },
      {
      	name:'news',
      	path:'news',
      	component: () => import('@/views/HomeNews')
  	  },
      {
       name:'messages',
      	path:'messages',
      	component: () => import('@/views/HomeMessages')     
      }
      ]
      
  },
  {
    name:'about',
    path:'/hbout',
    component:()=> import('@/views/about')
  }
]

export default routes;
```

