/request

```js
import axios from 'axios';

export  function instance(config){
  	//创建基础axios实例
     const instance1 = axios.create({
         baseURL:'',
         timeout:1000
     });
		//创建请求拦截器
     instance1.interceptors.request.use( config => {
        return config
     },err=>{
        console.log(err)
     })
  	//创建响应拦截器
     instance1.interceptors.response.use( res => {
         return res;
     },err=>{
         console.log(err)
     })
     return instance1(config)
    } 
```

