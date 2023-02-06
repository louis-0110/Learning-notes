## I/O:input output

对外部设备的输入输出

外部设备

IO的速度往往低于内存和cpu的交互速度



## FS

1. readFile 读文件 （readFileSync 同步 一般用于初始化操作，会阻塞代码执行）

```js
const { readFile ，promises } = require('fs')

//fs.readfile()

readFile(
  path.resolve(__dirname, './server.js'),
  {
    encoding: 'utf-8',
  },
  (err, content) => {
    console.log(content)
  }
)

//
promises.readFile()
```

2. writeFile 写文件

3. stat 文件详情  .isDirectory() .isFile()  true / false 是否是目录

4. readdir() 返回文件夹里面的子文件名/子文件夹名

5. mkdir() 创建目录

6. access() 访问权限

7. unlink() 删除文件

```js
fs.stat(path.resolve(__dirname, './src/assets'), (err, state) => {
  console.log(state.isDirectory(), state.isFile())
})

fs.readdir(path.resolve(__dirname, './src/'), (err, state) => {
  console.log(state) //[ '.DS_Store', 'abc.cjs', 'assets', 'test.cjs' ]
})

```

