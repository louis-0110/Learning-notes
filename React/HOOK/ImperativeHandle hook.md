# ImperativeHandle hook

在函数组件的实例上添加东西，方便在父组件中使用



```jsx
import {useRef,useImperativeHanle} from 'react'


function Test(props,ref){
  useImperativeHandle(ref,()=>{
		return {
      method(){
        console.log('eeee')
      }
    }    
  },[])
  
  return <span>22</span>
}

const TestRef = React.forwardRef(Test)

function P(){
	const ref = useRef()
  
  return <>
  	<TestRef ref={ref}/>
    <button onClick={()=>{
        ref.current.method() // eeee
      }}>点击</button>
  </>
}


```

