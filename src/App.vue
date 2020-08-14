<template>
  <div id="app">
    {{todos}}
    <todos v-model="todos"/>
    <button @click="addTodo()">Ajouter une tâche</button>
  </div>
</template>

<script>
import Todos from './components/Todos'


export default {
  data () {
    return {
      // todos:[{
      //   // name: 'Demo',
      //   // completed: true
      // }]
    }
  },
  methods: {
    addTodo() {
      this.todos.push({
        name:'Jean',
        completed: false
      })
    }
  },
  name: 'App',
  components: {
    Todos
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
