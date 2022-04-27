```js
toLocaleString(locale, options)

//千分位显示
const num = 123456.456; 
num.toLocaleString(num) //'123,456.456'

//显示.00
const num = 236; 
num.toLocaleString('zh',{minimumFractionDigits: 2 }) //'236.00'

//百分显示
const num = 0.123;
num.toLocaleString('zh',{style:'percent',minimumFractionDigits: 2 }) //12.3%

//数字转化为货币表示法
const num = 236; 
num.toLocaleString('zh',{style:'currency',currency:'cny' }) //'¥236.00'

```



