### 字符串转base64

```js

//字符串转base64
function encode(str) {
  // 对字符串进行编码
  var encode = encodeURI(str);
  // 对编码的字符串转化base64
  var base64 = window.btoa(encode);
  return base64;
}

// base64转字符串
function decode(base64) {
  // 对base64转编码
  var decode = window.atob(base64);
  // 编码转字符串
  var str = decodeURI(decode);
  return str;
}
```



### base64 转 blob

```js
//blob 转 base64
function blobToDataURI(blob, callback) {
   var reader = new FileReader();
   reader.readAsDataURL(blob);
   reader.onload = function (e) {
       callback(e.target.result);
   }
}

//base64 转 blob

 function dataURItoBlob(base64Data) {
     //console.log(base64Data);//data:image/png;base64,
     var byteString;
         byteString = atob(base64Data.split(',')[1]);//base64 解码
     var mimeString = base64Data.split(',')[0].split(':')[1].split(';')[0];
   	 //mime类型 -- image/png
     // var arrayBuffer = new ArrayBuffer(byteString.length); //创建缓冲数组
     // var ia = new Uint8Array(arrayBuffer);//创建视图
     var ia = new Uint8Array(byteString.length);//创建视图
     for(var i = 0; i < byteString.length; i++) {
         ia[i] = byteString.charCodeAt(i);
     }
     var blob = new Blob([ia], {
         type: mimeString
     });
     return blob;
 } 

```

