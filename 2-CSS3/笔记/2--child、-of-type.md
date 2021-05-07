## -child

> -child类型的选择器都会被其他的元素影响,会加上其他兄弟元素一起算顺序

1. Ele:first-child (选中Ele元素是父级的第一个子元素，父级的第一个子元素是其他元素就不会被选中 )
2. Ele:last-child (选中Ele元素是父级的最后一个子元素，父级的最后一个子元素是其他元素就不会被选中 )
3. Ele:onle-child (选中Ele元素是父级仅有的一个子元素，父级中还有其他元素就不被选中 )
4. Ele:nth-child(n)（顺序选中子元素为n的Ele元素，不是就不会选中）n为1选中第一个 等同于first-child
5. Ele:nth-last-child(n)（倒序选中子元素为n的Ele元素，不是就不会选中）n为1选中最后一个 等同于last-child

```html
<div>
  <a>a-1</a>
  <p>p-1</p>
  <p>p-2</p>
  <p>p-3</p>
  <p>p-4</p>
  <p>p-5</p>
</div>
```

```css
p:first-child{ // 没有任何p元素被选中，因为a是第一个子元素
  
}
p:last-child{ // p-5 被选中
  
}
p:nth-last-child(2){ //p-4 被选中
  
}
p:nth-child(odd){//odd奇数 even偶数
  //p-2 p-4
}
p:nth-child(n+2){//
  //p-1 p-2 p-3 p-4 p-5
}
```

## -of-type

> 不会受到其他元素的影响,只会算Ele元素自己的顺序，不会带上别的元素

1. Ele:first-of-type (选中所有Ele元素中的第一个子元素 )
2. Ele:last-of-type (选中所有Ele元素中的最后一个子元素 )
3. Ele:onle-of-type (选中父级中只有一个Ele元素，Ele可以有其他兄弟元素)
4. Ele:nth-of-type(n)（顺序选中Ele元素中为n的Ele元素，不是就不会选中）n为1选中第一个 等同于first-of-type 
5. Ele:nth-last-of-type(n)（倒序选中Ele元素为n的Ele元素，不是就不会选中）n为1选中最后一个 等同于last-of-type

```css
<div>
  <a>a-1</a>
  <p>p-1</p>
  <p>p-2</p>
  <p>p-3</p>
  <p>p-4</p>
  <p>p-5</p>
</div>
```

```css
p:first-of-type{ // p-1 被选中
  
}
p:last-of-type{ // p-5 被选中
  
}
p:nth-last-of-type(2){ //p-4 被选中
  
}
p:nth-of-type(odd){//odd奇数 even偶数 
  //p-1 p-3 p-5 会被选中
  
}
p:nth-of-type(n+2){//odd奇数 even偶数
  //p-2 p-3 p-4 p-5
}
```

