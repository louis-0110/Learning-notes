## Memo hook

用于保持一些比较稳定的数据，通常用于性能优化。(复杂计算得到的值)

首次渲染会执行， 返回一个值，并固定它。只有当依赖项改变时，才会重新执行，返回新的值

**如果React元素本身的引用没有发生变化，一定不会重新渲染**

```jsx
import {useMemo} from 'react'

function Parent(){
  const [txt,setTxt] = useState();
  
  const onHandle = useMemo(()=>{
  return ()=> {setTxt(Math.random)}
},[txt])
  
  return (
  	<div>
    	<Test onClick={onHandle}></Test>
    </div>
  )
}
```

