

# flex

### 在父级元素设置的属性

display:flex; 

> 将对象作为弹性伸缩盒显示。（伸缩盒最新版本）（CSS3）

display:inline-flex;

> 将对象作为内联块级弹性伸缩盒显示。（伸缩盒最新版本）（CSS3）



给一个元素设置 **dispaly:flex;** 让这个元素内部变成flex布局

这个元素可以设置 **flex-direction** （主轴/交叉轴） 

**flex-wrap** 换行方式

基于主轴对齐方式（默认水平对齐方式） **justify-content**  

基于交叉轴对齐方式（默认垂直方向对齐方式） **align- content**（必须作用到多行元素）

**align-items**  (单行元素) 

flex-start

flex-end

Center

Baseline  文本基线

 默认：Stretch 子项不设置高度 ，子项高度就会自动撑满父级

```css
.wrap{
  width:400px;
  heigth:300px;
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  align-items:center;
  align-content:center;
}
.wrap > div{
  
}
```



tips：**resize:both;必须和overflow 配合使用**

### 在子集元素设置的属性

order ： 用整数值来定义排列顺序，数值**小**的排在前面。可以为**负值**。默认值：0

align-self：设置或检索弹性盒子元素自身在**侧轴**（纵轴）方向上的对齐方式。align-content > align-self > align-item



 **flex**：none | <' [flex-grow] '> <' [flex-shrink] >'? || <' [flex-basis]'>  (伸 缩 基础 )

1. flex: none;  = flex : 0 0 auto;

```css

```

[flex-basis]：== width 

flex-basis 会被文本撑开宽度；width文本会超出到后面元素的下面

只写basis，代表元素的最小宽度 设置了width 并且 basis小于width

 basis < realwidth < width