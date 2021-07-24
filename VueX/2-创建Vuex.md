## 创建Vuex

1. npm i vuex

2. 引入vuex

   ```js
   - store/index.js
   
   	import vue from 'vue';
     import Vuex from 'vuex';
   	
   	vue.use(Vuex);
   export default new Vuex.Store({
     state:{
       count:0
     },
     mutations,
     actions,
     getters,
     moduls:{
       a:modulesA,
       b:modulesB
     }
   })
   ```

3. 引入 store

    ```js
    - main.js
    	import store from '@/store';
    	
    	new Vue({
        el:'#app',
        store
      })
    ```

