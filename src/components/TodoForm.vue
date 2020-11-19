<template>
  <form @submit.prevent="onSubmit">
    <Input />
    <AddTodoButton 
      v-bind:addTodo="addTodo"
    />
  </form>
</template>


<script>
import AddTodoButton from './AddTodoButton'
import Input from './Input'
export default {
  props: ['todos', 'addTodo'],
  components: {
    AddTodoButton,
    Input,
  }
}
</script>
