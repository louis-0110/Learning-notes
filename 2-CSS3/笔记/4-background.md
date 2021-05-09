# background

1. bakcground-image

```css
background-image:url(),url(); //容错 后面的在下面
```

2. background-repeat 

   - repeat-x：背景图像在横向上平铺

   - repeat-y：背景图像在纵向上平铺

   - repeat：背景图像在横向和纵向平铺

   - no-repeat：背景图像不平铺

   - round：当背景图像不能以整数次平铺时，会根据情况缩放图像。（CSS3）

   - space：当背景图像不能以整数次平铺时，会用空白间隙填充在图像周围。（CSS3）

```css
background-repeat:no-repeat;
```

3. background-origin：border-box； padding-box content-box

设置背景图片从那里开始渲染的 默认是padding-box 

```css
div{
  background-origin:border-box;
}
```

4. background-clip:text; (border-box padding-box content-box text)

设置背景图片在什么地方截断

```css
div{
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent; //设置文字颜色透明 也可以用color:transpatent;
}
文字透明背景
```

5. background-position

   **指定背景图像在元素中出现的位置。**

   - 百分比 %
   - 长度值 px

   - center：背景图像横向或纵向居中。

   - left：背景图像从元素左边开始出现。

   - right：背景图像从元素右边开始出现。

   - top：背景图像从元素顶部开始出现。

   - bottom：背景图像从元素底部开始出现。

> 如果只提供一个，该值将用于横坐标；纵坐标将默认为50%（即center）。

```css
background-position:center center;

background-position:0 0 ;

background-position: 0 ; 等同于 background-position: 0 center;
background-position: center center 10px;
background-position: center 20px bottom 20px;
```

