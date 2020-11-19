<template>
  <div>

    <TodoList 
      v-bind:todos="todos"
    />
    <AddTodoButton 
      v-bind:addTodo="addTodo"
    />
  </div>
</template>

<script>
import TodoList from './TodoList'
import AddTodoButton from './AddTodoButton'
export default {
  props: ['todos', 'addTodo'],
  components: {
    TodoList,
    AddTodoButton,
  }
}
</script>
