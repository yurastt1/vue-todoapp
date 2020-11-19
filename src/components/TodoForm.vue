<template>
  <form @submit.prevent="onSubmit">
    <Input />
    <AddTodoButton />
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
  },
   data() {
    return {
      
    }
  },
    methods: {
    onSubmit() {
      const todo={id: 3, title: 'sex', status: 'completed'}
      this.addTodo(todo)

    }
  }
}
</script>
