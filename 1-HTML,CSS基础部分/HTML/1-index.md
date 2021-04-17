# 元素

```html
<a href='http://www.baidu.com' title='百度一下' >百度一下</a>
<title>页面标题</title>
```

元素 = begin tag + end tag + element content + element attribute

属性 = 属性名 + 属性值


属性的分类：
    -局部属性：某些元属的特有属性   checked  href src 
    -全局属性：所有元素都能用的属性    title  id class lang

## 空元属 （单标签）

```html
    <meta charset='utf-8'>
    <img src='xxx.png'>
```

```html
    <html lang='cmn-hans en'> 

```
lang属性：language ，全局属性，表示该元属内部使用的文字是哪一种自然语言书写的内容(中文：cmn-hans  英文：en)

```html
    <meta charset="UTF-8">
```
    文档的元数据：附加信息

# 语义化

a元属：超链接
p元素：段落
h1元素：1级标题

元素展示到页面中的效果，应该由css决定

因为浏览器自带有默认的css样式，所以每个元属有一些默认的样式

**重要：选择什么元素，取决于内容的含义，而不是显示的效果**

## pre

 预格式化文本
 ```html
 <pre> lorem ！lorem～ </pre>
 ```
 默认的css：white-space：pre
 > 显示代码时用code元素；或者加 white-sapce：pre;







