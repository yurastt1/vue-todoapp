<template>
  <form @submit.prevent="onSubmit">
    <input v-model="title" />
    <button 
      type="submit"
      value="Submit"
      :disabled="!title"
    >add task </button>
    <span v-if="errorByLength">Максимальна довжина пункту - 30 символів</span>
    <span v-if="errorIsAdded">Вже додано</span>
    <span v-if="errorIsAdded">Успішно видалено</span>
  </form>
</template>


<script>
// import AddTodoButton from './AddTodoButton'
// import Input from './Input'
export default {
  props: ['todos', 'addTodo'],
  components: {
    // AddTodoButton,
    // Input,
  },
   data() {
    return {
      title: '',
      isDisabled: true,
      errorByLength: false,
      errorIsAdded: false,
    }
  },
    methods: {
    onSubmit() {
      if (this.title.length > 30) {
        this.errorByLength = true;
        setTimeout(() =>  this.errorByLength = false, 5000);
        return
      }
       if (this.todos.some(element => element.title === this.title)) {
        this.errorIsAdded = true;
        setTimeout(() =>  this.errorIsAdded = false, 5000);
        return
      }

      const todo={id: 3, title: this.title, status: 'completed'}
      this.addTodo(todo)

      this.title = ''
    }
  }
}
</script>
