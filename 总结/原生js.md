## 判断 对象是不是空

1. JSON.stringify()
2. Object.keys()



```js
var data = {};
var b = (JSON.stringify(data) == "{}");
alert(b);   //true 为空， false 不为空`

var data = {};
var arr = Object.keys(data);
alert(arr.length == 0); //true 为空， false 不为空
```

