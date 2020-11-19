<template>
  <div id="app">
    <TodoApp 
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
 
  // methods: {
  //   addTodo(todo) {
  //     this.todos = [...this.todos, todo]
  //   },
  //   deleteItem(item) {
  //     const deleteItemIndex = this.todos.findIndex(element => element.title === item)
  //     this.todos.splice(deleteItemIndex, 1);
  //   }
  // }
}
</script>
