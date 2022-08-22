### Node 模块化细节

1. 模块的查找

   1. 绝对路径

   2. 相对路径 ./ 或 ../

   3. 相对路径 

      i.检查是否是内置模块，如 fs 、path等

      ii. 检查当前目录中的node_modules

      iii. 检查上级目录中的node_modules 

      iiii. 转换成绝对路径 加载模块 （都没有找到，就报错误）

   4. 关于后缀名 - 如果不提供后缀名会自动补全 js 、json、node、mjs

   5. 关于文件名 -如果只提供目录名没有提供文件名 会自动找 index文件 package.json中main 指定入口

2. module对象

3. require函数

```js
console.log(require.resolve('./server.js'))
console.log(path.resolve('./server.js'))
```

###  module.exports

模块里面 const exports = module.exports

this = module.exports



### es 模块化

使用 esModule的方法：

1. 文件名 改成 .mjs

2. 最近的package.js type改成module

运动 esModule

运行 node --experimental-modules index.js

