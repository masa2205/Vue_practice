<template>
  <div class="hello">
    <ol>
      <li v-for="todo in todos">
        {{ todo.text }}
      </li>  
    </ol>  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      todos: [
        {text:'Learn JavaScript'},
        {text:'Learn Vue'},
        {text:'Build something awesome'}
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
