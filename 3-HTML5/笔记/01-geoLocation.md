## 获取地理信息

```js
window.navigator.geolocation.getCurrentPosition(position=>{
  
},err=>{
  
})
```

1. 有 `gps` 移动端手机 通过`gps`获取定位

2. 没有 `gps` 台式电脑，笔记本电脑 通过网络获取定位
   1. `https://` 协议
   2. `files://` 协议
   3. 在chrome浏览器里面`定位提供商是goole` ，要`翻墙`才能获取到位置信息

