## Object的新增API

1. Object.is

用于判断两个数据是否相等，剧本上跟严格相等（===）是一样的，除了: 

1) NaN === NaN

2) -0 === +0



2. Object.assign

用于混合对象

```js
const obj1 = {
  a:123,
  b:456,
  c:'abc'
}
const obj2 = {
  a: 123,
  b: 456,
  d: 'ddd'
}

Object.assign({},obj1,obj2)
// 以第一个对象为基础，混合后面的对象相同属性名后面覆盖前面的，最后返回第一个对象（引用）
{
	a:123,
 	b:456,
  c:'abc',
  d:'ddd'
}
```

3. Object.getOwnPropertyNames  的枚举顺序

   >  输出对象属性值的数组，先按生序排数字，后按书写顺序排其他

```js
const obj = {0:"sfs",10:"adsfa",4:'adsfa',ab:'adsfa',sadf:'sdfgjea'}
Object.getOwnPropertyNames(obj)

(5) ["0", "4", "10", "ab", "sadf"]
```

3. Object.setPrototypeOf

   设置对象的隐式原型

   

```js
老的方法是：obj.__proto__ = obj2
```

```js
Object.setPrototypeOf(obj,obj2)
```

