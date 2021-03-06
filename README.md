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
***
<br/>

### 条件分技
```html
<div class="hello">
  <span v-if="seen">
    Now you see me
  </span>  
</div>
```
```js
data () {
  return {
    seen:true
  }
}
```
***

<br/>

### ループ
```html
<div class="hello">
  <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>  
  </ol>  
</div>
```
```js
data () {
  return {
    todos: [
      {text:'Learn JavaScript'},
      {text:'Learn Vue'},
      {text:'Build something awesome'}
    ]
  }

}
```
***
<br/>

### ユーザー入力の制御(v-on)
```html
<div class="hello">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">Reverse Message</button>
</div>
```
```js
data () {
  return {
    message: 'Hello Vue.js!'
  }
},  
methods: {
  reverseMessage: function () {
    this.message = this.message.split('').reverse().join('')
  }
}
```
***
<br/>

### ユーザー入力の制御(v-model)
```html
<div class="hello">
    <p>{{ message }}</p>
    <input v-model="message">
  </div>
```
```js
data () {
    return {
      message: 'Hello Vue.js!'
    }
  }
```
***
<br/>

### コンポーネントによる構成
```html
<template>
  <div class="hello">
    <ol>
      <todo-item
        v-for="item in grocerylist"
        v-bind:todo="item"
        v-bind:key="item.id"
      ></todo-item>  
    </ol>  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      groceryList: [
        { id: 0, text: 'Vegetables' },
        { id: 1, text: 'Cheese' },
        { id: 2, text: 'Whatever else humans are supposed to eat' }
      ]
    }
  }
}  
</script>
```
```js
Vue.component('todo-item', {
  props: ['todo'],
  template: '<li>{{ todo.text }}</li>'
})
```
***
<br/>

# Vueインスタンスの作成
```js
var vm = new Vue({
  // オプション
})
```
***
<br/>

# テンプレート構文

<br />

## 展開

***

### テキスト
Mustache構文を利用したテキスト展開
```html
<span>Message: {{ msg }}</span>
```

<br />

生のHTML
```html
<p>Using mustaches: {{ rawHtml }}</p>
<p>Using v-html directive: <span v-html="rawHtml"></span></p>
```