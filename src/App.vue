<template>
  <div id="app">
    <TodoApp 
      v-bind:todos="todos"
      v-bind:addTodo="addTodo"
    />
  </div>
</template>

<script>
import TodoApp from './components/TodoApp'
export default {
  name: 'App',
  components: {
    TodoApp
  },
  data() {
    return {
      todos: [{id: 1, title: 'mama', completed: true}, {id: 2, title: 'pups', completed: false}]
    }
  },
  methods: {
    addTodo(todo) {
      this.todos = [...this.todos, todo]
    },
  }
}
</script>
