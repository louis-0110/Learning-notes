## 数据双向绑定 v-model

```vue
<!-- vue2 -->
<ChildComponent :value = 'pageTitle' @input='pageTitle = $event' />
<! --简写 -->
<ChildComponent v-model='pageTitle' />


<!-- vue3 -->
<ChildComponent
  :modelValue='pageTitle'
  @update:modeValue='pageTitle = $event'
/>

<!-- 简写为 -->
<ChildComponent v-model='pageTitle' />
```

多个双向绑定

```vue
<!-- vue2 -->
<ChildComponent v-model='pageTitle' :text.sync='someText'/>

<!-- vue3 -->
<!-- 简写为 -->
<ChildComponent v-model='pageTitle' v-model:text='someText'/>
```

