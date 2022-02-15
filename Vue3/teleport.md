## teleport

传输html到指定的元素内



```vue
- App.vue

<TestTeleport />


-Test-teleport.vue

<div>
    <button @click="showModal = true">点击</button>
    <teleport to="body">
      <div v-show="showModal" class="modal-button">
        <button @click="showModal = false">关闭</button>
      </div>
    </teleport>
  </div>


->>
<html>
  <head></head>
  <body>
    ....... some element
    <div class='modal-button'>
      <button>.....</button>
    </div>
  </body>
</html>
```