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
  props: ['todos', 'addTodo'],
  components: {
    TodoList,
    TodoForm,
  },
  methods: {
    deleteItem(event) {
      console.log(event);
    }
  }
}
</script>
