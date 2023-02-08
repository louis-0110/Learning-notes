## http请求

1. 普通模式 ： 三次握手 数据请求 数据响应 四次挥手

2. 长链接模式：  三次握手 各种数据传输  四次挥手

    Request Headers   keep-alive 保持连接

<img src="https://tva1.sinaimg.cn/large/e6c9d24egy1h5gsie1b7wj215y0rgwkc.jpg" alt="image-20220823164130525" style="zoom:50%;" />



## net模块能干什么

net是一个通信模块，利用它可以实现 进程间的通行 IPC ，**网络通信 TCP/IP**



## 创建客户端

```ts
const net = require('net')

//返回socket
const socket = net.createConnection({
  host:'duyi.ke.qq.com',
  port:80
},()=>{
  console.log('链接成功')
})

socket.on('data',chunk =>{
  console.log('')
})
               
```

> socket ： socket 是一种特殊的文件，在node中表现为一个双工流对象，通过向流写入内容发送数据，通过监听流的内容获取数据



## 创建服务器

```ts
const net = require('net')

// 返回server对象
const server = net.createServer();

server.listen(12306) //服务器监听端口

server.on('listening',()=>{
  
})

// 当被客户端链接
server.on('connection',(socket)=>{
  
})
```

![image-20230207173741158](https://p.ipic.vip/prhfzr.png)
