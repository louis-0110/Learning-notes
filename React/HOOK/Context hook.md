## context hook

获取上下文数据

```tsx
import {useContext} from 'react'

const ctx = React.createContext()

functino Test(){
  const value = useContext(ctx)
  return <h1>Test,上下文的值:{value}</h1>
}

export default function App(){
  return (
  	<div>
    	<ctx.Provider value='abc'>
      	<Test/>
      </ctx.Provider>
    </div>
  )
}
```

