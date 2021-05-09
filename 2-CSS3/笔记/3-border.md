## border

#### border-radius

```css

div{
  border-radius:50%;
  
  border-top-left-radius:55pt 25pt; // 左上
  border-top-right-radius:55pt 25pt; // 右上
  border-bottom-right-radius:55pt 25pt; // 右下
  border-bottom-left-radius:55pt 25pt; // 左下
  
}

```

![水平与垂直半轴](http://css.doyoe.com/properties/backgrounds/images/corner.png)

**能看到此时 55pt 被应用于椭圆的水平半轴，25pt 被应用于垂直半轴。**



#### box-shadow

```css
box-shadow: x偏移 y偏移 blur 放大 #fff;

box-shadow: inset x偏移 y偏移 blur  放大 #fff; 内阴影
```

#### border-image



1. [border-image-source](http://css.doyoe.com/properties/backgrounds/border-image-source.htm)：

定义元素边框背景图像，可以是图片路径或使用渐变创建的“背景图像”。

```css
div{
  width:100px;
  height:100px;
  position:absolute;
  left:calc(50% - 50px);
  top:calc(50% - 50px);
  border:10px solid ;
  border-color:Lightpink; 
  background-image-source:linear-gradient(red, yellow);
  background-image-slice:10; //必须写
}
```

<img src="https://tva1.sinaimg.cn/large/008i3skNgy1gqbdd8yh1tj30by07et8z.jpg" style="zoom:50%;"/>

2. [border-image-slice](http://css.doyoe.com/properties/backgrounds/border-image-slice.htm)：

定义元素边框背景图像从什么位置开始分割。

```css
border-image-slice:top left bottom right; 默认值 100%
```

<img src="https://tva1.sinaimg.cn/large/008i3skNgy1gqbdr1pu56j3029029t8o.jpg"/>

![](https://tva1.sinaimg.cn/large/008i3skNgy1gqbe5krvoxj30as08gdg9.jpg)

3. [border-image-width](http://css.doyoe.com/properties/backgrounds/border-image-width.htm)：

定义元素边框背景图像厚度。

4. [border-image-outset](http://css.doyoe.com/properties/backgrounds/border-image-outset.htm)：

定义元素边框背景图像的外延尺寸。

5. [border-image-repeat](http://css.doyoe.com/properties/backgrounds/border-image-repeat.htm)：

定义元素边框背景图像的平铺方式。

