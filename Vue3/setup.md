## setup

```js
// MyBook.vue

export default {
  props: {
    title: String
  },
  setup(props,context) {
    console.log(props.title)
    const {emit , slots,  attrs} =  context;
  }
}
```