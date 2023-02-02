# 为网页添加样式

# 术语解释

```css
h1{
    color:red;
    background-color:lightblue;
    text-align: center;
}
```

Css规则 = 选择器 + 声明块 

### 选择器

 选择器：选中元素

 1. ID选择器：选中的是对应的id值得元素   (#id)
 2. 元素选择器   (div span p )
 3. 类选择器    （.class



 ### 声明块
 出现在{ }中     


 ## CSS代码书写位置

内部样式表 
```html
<style>
    
</style>
```

内联样式
```html
<div style='width:100px;' > </div>
```

外部样式表[推荐]
```html
<link href='index.css'>
```

1).外部样式可以解决多页面样式重复的问题
2).有利于浏览器缓存，从而提高页面响应速度
3).有利于代码分离（HTML和CSS），更容易阅读和维护
