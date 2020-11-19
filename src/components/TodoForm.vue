<template>
  <form @submit.prevent="onSubmit">
    <input v-model="title" />
    <AddTodoButton v-bind:title="title" />
  </form>
</template>


<script>
import AddTodoButton from './AddTodoButton'
// import Input from './Input'
export default {
  props: ['todos', 'addTodo'],
  components: {
    AddTodoButton,
    // Input,
  },
   data() {
    return {
      title: '',
      isDisabled: true,
    }
  },
    methods: {
    onSubmit() {
      if (this.title.length === 0) {
        console.log(21);
        return
      }
      const todo={id: 3, title: this.title, status: 'completed'}
      this.addTodo(todo)

      this.title = ''
    }
  }
}
</script>
