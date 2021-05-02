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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
