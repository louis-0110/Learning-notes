## image 空元素 图片元素

##### 属性

`src`: 图片路径 source 资源

`title`: 图片提示符

`alt`:图片占位符 当图片资源失效的时候显示的文字

```html
<img src='path/xxx.png'/>
```




## map元素
```html
<img usemap='#solarMap'>
<map name='solarMap'>
    <area shape='circle' coords='圆心坐标 X，Y ，R' href='' target=''>
    <area shape='rect' coords='左上角坐标，右下角坐标' href='' target=''>
    <area shape='poly' coords='x,y,x,y,x,y,x,y,x,y' href='' target=''>
</map>
```


## 和figure 元素
把图片元素 和 其他的元素包起来 表示 所有的元素和图片相关
子元素： figcaption  figure的标题

```html
<figure>
    <figcaption>
        <h2>标题</h2>
    </figcaption>
    <img usemap='solarMap' src=''>
    <map name='solarMap'>
    <area shape='circle' coords='圆心坐标 X，Y ，R' href='' target=''>
    <area shape='rect' coords='左上角，右下角' href='' target=''>
    <area shape='poly' coords='x,y,x,y,x,y,x,y,x,y' href='' target=''>
		</map>
</figure>
```