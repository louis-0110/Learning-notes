## slot



1. 使用插槽  <slot></slot>

```vue
-子组件cnp
<div>
   <a>123</a>
  <slot></slot>
</div>

-父组件
<div>
  <cnp/>
</div>

//123
```



2. 插槽的默认值 <slot><p>当没有在组件中传入插槽时，默认显示的元素</p> </slot>

```vue
-子组件cnp
<div>
   <a>123</a>
  <slot>
    <p>abc</p>
  </slot>
</div>

-父组件
<div>
  <cnp/>
</div>

// 123
// abc
```



### 具名插槽

```vue
-子组件cnp
<div>
   <a>123</a>
  
  <slot>
   <p>abc</p>
  </slot>
  
  <slot name='left'>
    <p>abc</p>
  </slot>
  
  <slot name='right'>
  </slot>
  
</div>

-父组件
<div>
  <cnp>
    <template #left>
			<span>left</span>
    </template>
    <template #right>
			<span>right</span>
    </template>
  </cnp>
</div>

```

### 作用域插槽 

用途：父组件替换插槽的标签，内容由子组件提供，

在使用组件的时候，父级拿到子组件的数据

```vue
-子组件cnp
<div>
  <slot>
  </slot>
  <slot name='left' v-bind:user='user'>
  </slot>
  <slot name='right' :user='user'>
  </slot>
</div>


-父组件
<div>
  <cnp v-slot='{user}'> // v-slot:default='slotProps'  #default='slotProps' (独占默认插槽的写法，只有默认一个默认插槽的时候可以这么用)
    <template #left='{user}'> (常规作用域插槽的写法)
			<span>{{user.name}}</span> //slotProps.user.name slotProps.user.name
    </template>
    <template #right>
			<span>{{user.age}}</span> //slotProps.user.name slotProps.user.name
    </template>
    
  </cnp>
</div>
```

![image-20220331165829732](https://tva1.sinaimg.cn/large/e6c9d24egy1h0t659u98sj214e0i8jt2.jpg)

