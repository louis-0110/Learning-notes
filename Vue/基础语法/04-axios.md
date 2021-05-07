```js
import axios from 'axios';

export  function instance(config){
     const instance1 = axios.create({
         baseURL:'',
         timeout:1000
     });

     instance1.interceptors.request.use(config=>{
        return config
     },err=>{
        console.log(err)
     })
     instance1.interceptors.response.use(res=>{
         return res;
     },err=>{
         console.log(err)
     })
     return instance1(config)
    } 
```