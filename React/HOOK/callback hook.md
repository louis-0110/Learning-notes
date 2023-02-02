## useCallback hook

简介：用于得到固定函数的引用值的hook

1. 第一参数是函数
2. 第二个参数是依赖项
3. 返回值，相对固定的函数引用

```tsx

class Test extent React.PureComponent{
  constructor(){
    
  }
  
  render(){
    return (
    	<div> </div>
    )
  }
}

function Parent(){
  const [txt,setTxt] = useState();
  
  const onHandle = useCallback(()=>{
  setTxt(Math.random)
},[])
  
  return (
  	<div>
    	<Test onClick={onHandle}></Test>
    </div>
  )
}
```

