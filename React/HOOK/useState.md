# state Hook

```tsx
import {useState} from 'react'

const [count , setCount] = useState(0)
```



# State Hook 原理

1. 当运行一个函数组件时，



**注意的细节**

1. useState最好写在函数的起始位置，便于阅读
2. useState严禁出现在代码块（判断，循环）中
3. useState返回的函数，引用不变（节约内存空间）
4. 使用函数改变数据，若数据和之前的数据完全相等，不会导致重新渲染。（使用 ```Object.is( )```比较）
5. 使用函数改变数据，传入的值不会和原来的数据进行合并，而是直接替换。
6. 如果要实现强势刷行组件
   1. 类组件：使用this.forceUpdate()
   2. hook中：使用一个空对象的useState()  ```const [,forceUpdate] = useState({}) ;    forceUpdate()```

7. **如果某些状态之间没有必然的联系，应该分化为不同的状态，而不要合并成一个对象**
8. 和类组件的状态一样，函数组件中改变状态可能是异步的（在DOM事件中），多个状态变化会合并以提交效率，此时不能信任之前的状态要使用回调函数

```tsx

import {useState} from 'react'

const [count , setCount] = useState(0)

setCount((prev) => prev + 1)
```

