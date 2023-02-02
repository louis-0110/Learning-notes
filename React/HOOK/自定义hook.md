## 自定义hook

将一些常用的，跨越多个组件的hook功能，抽离出形成一个函数，该函数就是自定义hook

1. 函数名必须以use开头

2. 要放在开头，不能放在循环或判断中

ex：

1. 很多组件都需要在第一次加载完成后，获取所有学生数据
2. 很多组件都需要在第一次加载完成后，启动一个计时器，然后在组件销毁时卸载





```tsx
import {useEffect,useState} from 'react'
import {getAllStudents} from '@/api'

export default function useAllStudents(){
	const [students,setStudents] = useState([])
	useEffect(()=>{
    (async ()=>{
      	const stus = await getAllStudents();
      	setStudents(stus)
    })()
  },[])
  return students
}
```

