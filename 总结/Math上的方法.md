[`Math.trunc(x)`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc)

返回一个数的整数部分，直接去除其小数点及之后的部分。

[`Math.round(x)`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/round)

返回四舍五入后的整数。

[`Math.floor(x)`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)

返回小于一个数的最大整数，即一个数向下取整后的值。

[`Math.ceil(x)`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/ceil)

返回大于一个数的最小整数，即一个数向上取整后的值。

[`Math.abs(x)`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/abs)

返回一个数的绝对值。

[`Math.PI`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/PI)

圆周率，一个圆的周长和直径之比，约等于 `3.14159`。

```js
弧度角度转换
0 - 2PI  1 = 180/Pi

function degToRad(deg){
  return Math.PI/180*deg
}
function radToDeg(rad){
  return 180/Math.PI*rad
}
```

