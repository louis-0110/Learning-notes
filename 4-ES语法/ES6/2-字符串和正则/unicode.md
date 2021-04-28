# 文字编码

```js
const text = "𠮷"
```

## 更好的Unicode支持

 新flag：/ /u

使用码点匹配

```js
/^.$/.test("𠮷"); // false 匹配一个字符

/^.$/u.test("𠮷"); //true 匹配一个字符
```



## 更多的字符串API

实例方法：

- includes(prop, flag)
- startsWith(prop, flag)
- endsWith(prop, flag)
- repeat(prop, flag)



### 正则 - 粘连标志

标记名：y

含义：匹配时《完全按照正则对象中的lastIndex位置开始匹配，并且匹配的位置必须在lastIndex位置