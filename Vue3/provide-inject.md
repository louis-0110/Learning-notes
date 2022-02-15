## provide - inject



### provide 提供

```vue
import {provide, ref} from 'vue';

provide('name','xiaoming');
provide('age',19);
// 响应式

const name = ref('reactive 小明');
provide('name',name)

// 函数

provide('changeName',function(data){

})
```



### inject 注入

```vue
import {inject} from 'vue';

const name = inject('name','无名') //设置默认值

//响应式
const name = inject('name') // 

//函数
const changeName = inject('changeName');

changeName('xxxmingzi');

≥
```

