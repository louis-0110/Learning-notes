# a元素

- 超链接  

```html
<a href='https://www.baidu.com'>百度</a>
<a href='' target='_blank' rel="noopener noreferrer"></a>
```

## href属性 

1. 跳转地址
   2. 跳转到锚点

```html
<a href='#chapter'>锚点跳转</a>
<a href='#idname'>跳转到某个元素</a>

<p id='chapter'>lorem</p>
//回到顶部 直接写个 # 就能跳转到顶部
```
3. 功能链接/协议限定符
   点击后触发功能

   执行js代码，JavaScript:

```html
<a href='javascript:js代码'>
<a href = 'javascript:viod(0)'
```
-发送邮件，mailto:

-拨打电话，tel:

```html
<a href = 'tel:16655021802'></a>
<a href = 'mailto:574169815@qq.com'></a>
```

## taget属性

```css
target:self;//默认值 当前窗口打开
target:_blank; 在新窗口打开打电话
```