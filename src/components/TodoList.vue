<template>
  <ul>
    <TodoItem
      v-for="(todo, index) in todos" :key="index"
      v-bind:todo="todo"
    />
  </ul>
</template>

<script>
import TodoItem from './TodoItem'
export default {
  props: ['todos'],
  components: {
    TodoItem
  }
}
</script>
