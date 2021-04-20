#### 引入css的三种方式

1. link标签引入

```html
<html>
  <head>
    <title>Document</title>
    <link href="main.css" rel="stylesheet">
  </head>
</html>
```

2. 页面内style标签

```html
<html>
  <head>
    <style>
      .oDiv{
        width:100px;
        height:100px;
        background:red;
      }
    </style>
  </head>
</html>
```



3. 标签行间

```html
<div style='height:100px;width:100px;backgroundColor:red;'></div>
```

