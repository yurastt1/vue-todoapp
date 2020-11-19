<template>
  <div>
    <TodoForm 
      v-bind:addTodo="addTodo"
    />

    <TodoList 
      v-bind:todos="todos"
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
  }
}

</script>
