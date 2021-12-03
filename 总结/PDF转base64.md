##  input 上传 

```HTML
<input type="file" name="file" id="file" style="display: none;" accept="application/pdf" multiple>

```

- accept 允许上传文件的MIME格式
- multiple 允许一次上传多个
- single 只允许上传一个



 files[0].prototype -> File.prototype  -> Blob.prototype

1.获取文件数据 转换编码格式 **显示的话可以用base64 或者 blob两种方式**

```js
inpt.files[0].arrayBuffer().then(res => {
  // file 转 arraybuffer
  console.log(res)
}
```

```js
 // arraybuffer 转 base64 
function arrayBufferToBase64(buffer) {
     var binary = '';
     var bytes = new Uint8Array(buffer);
     var len = bytes.byteLength;
     for (var i = 0; i < len; i++) {
       binary += String.fromCharCode(bytes[i]);
     }
     return window.btoa(binary);
   }
```

```js
arraybuffer 生成blob链接
let blobData = new Blob([blob], {
      type: 'application/pdf'
    });
const url = window.URL.createObjectURL(blobData);
```

2. 下载 可以获取arrayBuffer 数据生成a标签下载

```HTML
  <embed src="" type="application/pdf" width="100%" height="100%"></embed>
  <object data="" type="application/pdf" width="100%" height="100%"></object>
	<iframe src="" frameborder="0" type="application/pdf"></iframe>

// 可以放base64 也可以放blob链接
```

```js

input.onchange = function(){
   inpt.files[0].arrayBuffer().then(res => {
      // em.src = "data:application/pdf;base64," + arrayBufferToBase64(res);
      var blob = new Blob([res], {
        type: 'application/pdf'
      })
      blob = window.URL.createObjectURL(blob)
      em.src = blob
				
     //1. 第一种直接用获取的arrayBuffer下载
      download(res);
     //2. 第二种通过ajax请求 把base64数据 转换成 arrayBuffer格式的数据 然后下载
      var c = new XMLHttpRequest;
      c.open("GET", "data:application/octet-stream;base64," + arrayBufferToBase64(res));
      c.responseType = "arraybuffer";
      c.onload = function (a) {
        download(c.response)
      }
      c.send()

    });
}
```

```js
// 下载的本质就是通过创建a元素 href链接到blob地址上获取数据，通过 onclick事件获取资源下载 要设置download属性 属性值是下载文件的名称
function download(blob, fileName = 'record.pdf') {
    let blobData = new Blob([blob], {
      type: 'application/pdf'
    });
    const url = window.URL.createObjectURL(blobData);//生成Blob链接
    const a = document.createElement('a');

    a.style = 'display: none';
    a.href = url;
    a.download = fileName;
    document.body.appendChild(a);
    a.click();

    document.body.removeChild(a)
    window.URL.revokeObjectURL(url) //删除缓存对象
  }
```

