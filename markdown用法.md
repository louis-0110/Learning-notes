# 一、标题

```markdown
#  这是一级标题
##  这是二级标题
###  这是三级标题
####  这是四级标题
#####  这是五级标题
######  这是六级标题
```

#  这是一级标题
##  这是二级标题
###  这是三级标题
####  这是四级标题
#####  这是五级标题
######  这是六级标题

# 二、字体

```
**这是加粗的文字**
*这是倾斜的文字*
***这是斜体加粗的文字***
~~这是加删除线的文字~~
```

**这是加粗的文字**
*这是倾斜的文字*
***这是斜体加粗的文字***
~~这是加删除线的文字~~



# 三、引用

```bash
>这是引用的内容
>>这是引用的内容
>>>>>>>>>>这是引用的内容
```

>这是引用的内容
>>这是引用的内容
>>
>>>>>>>>>>这是引用的内容



# 四、分割线

```bash
---
----
***
*****
```

---
----
***
*****



# 五、图片

```bash
![图片alt](图片地址 '图片title')

图片alt就是显示在图片下面的文字，相当于对图片内容的解释。
图片title是图片的标题，当鼠标移到图片上时显示的内容。title可加可不加


![blockchain](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/
u=702257389,1274025419&fm=27&gp=0.jpg "区块链")
```

# 六、超链接

```csharp
[超链接名](超链接地址 "超链接title")
title可加可不加
  
[简书](http://jianshu.com)
[百度](http://baidu.com)
```

# 七、列表

##### 无序列表

```undefined
- 列表内容
+ 列表内容
* 列表内容

注意：- + * 跟内容之间都要有一个空格
```

##### 有序列表

```undefined
1. 列表内容
2. 列表内容
3. 列表内容

注意：序号跟内容之间要有空格
```

##### 列表嵌套

**上一级和下一级之间敲三个空格即可**

1. xxxxx

* skdjfksd
* skdjfk
* sdkfj

2. sdjfksdjf
   1. sdf
   2. sdfs
   3. pdf

3. sdjfksdjf



# 八、表格

```ruby
表头|表头|表头
---|:--:|---:
内容|内容|内容
内容|内容|内容

第二行分割表头和内容。
- 有一个就行，为了对齐，多加了几个
文字默认居左
-两边加：表示文字居中
-右边加：表示文字居右
注：原生的语法两边都要用 | 包起来。此处省略

姓名|技能|排行
--|:--:|--:
刘备|哭|大哥
关羽|打|二哥
张飞|骂|三弟
```

| 姓名 | 技能 | 排行 |
| ---- | :--: | ---: |
| 刘备 |  哭  | 大哥 |
| 关羽 |  打  | 二哥 |
| 张飞 |  骂  | 三弟 |



# 九、代码

~~~go
 单行代码： `代码内容`

多行代码块：```
					```

`javascirpt`

```
      const obj = {
      name:'xiaoming',
      age:18
    }
```
~~~

`javascirpt`

```html
<div>
  html: markdown
</div>
```

```js
const obj = {
  name:'xiaoming',
  age:18
}
```

# 十、流程图

~~~php
```flow
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
&```
~~~

```flow
st=>start: 开始
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
&```
```