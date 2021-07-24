1. vue子路由刷新报错 Uncaught SyntaxError: Unexpected token <

   访问的是相对路径拿不到静态资源

   

   问题解决方法1：将在路由中引入的组件路径改为绝对路径，比如：

   ```js
   // 原来引入方式
   const a= () => import('./A/a.vue')
   // 将'./'改为'/'
   const a= () => import('/A/a.vue')
   ```

   

   问题解决方法2：修改vue.config.js文件  更改配置文件要重新编译才能生效

   ```js
   function resolve (dir) {
     return path.join(__dirname, dir) // path.join(_dirname)设置绝对路径
   }
   module.exports = {
     chainWebpack: (config) => {
       config.resolve.alias
         // 第一个参数：别名 第二个参数：路径
         .set('components', resolve('src/components'))
         .set('assets', resolve('src/assets'))
         .set('commonjs', resolve('src/commonjs'))
         .set('views', resolve('src/views'))
         .set('network', resolve('src/network'))
     },
     //  将原来的 publicPath: './'，改成
     publicPath: '/'
     // 这样便可以解决路由刷新出新 Uncaught SyntaxError: Unexpected token '<'
   }
   ```


   原文链接：https://blog.csdn.net/qq_41121649/article/details/108310202