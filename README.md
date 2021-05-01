# Vue.jsチュートリアル

## 宣言的レンダリング
```html
<div id="app">
  {{ message }}
</div>
```

```Js
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```
