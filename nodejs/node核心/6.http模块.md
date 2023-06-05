## http模块

> http模块建立在net模块之上, 无须手动管理socket，无须手动组装消息格式

```ts
// http.request(url[,optionns][,callback])

const http = require('http')

cosnt request = http.request('',{
  method:"GET"
},resp=>{
  console.log('服务器响应的状态码',resp.statusCode)
  console.log('服务器响应头',resp.headers)
})

request.end(); 

//http.createServer([options][,requestListener])

const server = http.createServer((req, res) => {
  console.log(req.headers, req.statusCode, req.statusMessage, req.method, req.url)
	res.write('123')
  res.end('<div><div/>')
})
server.listen(9527)

```

