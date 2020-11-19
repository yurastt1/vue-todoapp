<template>
  <div>
    <TodoForm 
      v-bind:addTodo="addTodo"
      v-bind:todos="todos"
    />
 
    <TodoList 
      v-bind:todos="todos"
      v-bind:deleteItem="deleteItem"
    />
  </div>
</template>

<script>
import TodoForm from './TodoForm'
import TodoList from './TodoList'
export default {
   data() {
    return {
      todos: [{id: 1, title: 'mama', completed: true}, {id: 2, title: 'pups', completed: false}]
    }
  },
  components: {
    TodoList,
    TodoForm,
  },
  methods: {
    addTodo(todo) {
      this.todos = [...this.todos, todo]
    },
    deleteItem(item) {
      const deleteItemIndex = this.todos.findIndex(element => element.title === item)
      this.todos.splice(deleteItemIndex, 1);
    }
  }
}
</script>
