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
***
<br />

### 要素の属性を束縛(バインディング)
```html
<div class="hello">
    <span v-bind:title="message">
      Hover your mouse over me for a few second 
      to see my dynamically bound title!
    </span>  
  </div>
```

```js
 data () {
    return {
      message: 'You loaded thid page on' + 
               new Date().toLocaleString()
    }
  }
```