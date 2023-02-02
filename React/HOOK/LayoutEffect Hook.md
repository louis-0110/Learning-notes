# LayoutEffect Hook

useEffect：渲染时间点是浏览器渲染完成之后执行

useLayoutEffect ：执行时间点是在 改变DOM之后到浏览器渲染之间

用法和useEffect一样

```jsx

function Test(){
  
  useLayoutEffect(()=>{
    
  },[])
}
```

