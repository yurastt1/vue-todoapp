<template>
  <ul class="todo-list">
    <TodoItem
      v-for="(todo, index) in todos" :key="index"
      v-bind:todo="todo"
      v-bind:deleteItem="deleteItem"
    />
  </ul>
</template>

<script>
import TodoItem from './TodoItem'
export default {
  props: ['todos', 'deleteItem'],
  components: {
    TodoItem
  }
}
</script>
