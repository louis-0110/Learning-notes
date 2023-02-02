## Ref hook

useRef函数：

1. 一个参数：默认值
2. 返回一个固定的对象 ```{current:值}```

```jsx

import {useRef,useEffect} from 'react'

function Test(){
  const timer = useRef(); //固定timer
  useEffect(()=>{
    timer.current = setInterval(()=>{
      
    },1000)
    
    return ()=>{
      clearInterval(timer.current)
    }
  })
  return <>
  	{}
  </>
}
```

