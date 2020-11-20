<template>
  <form @submit.prevent="onSubmit">
    <input v-model="title" />
    <button 
      type="submit"
      value="Submit"
      :disabled="!title"
    >
      add task 
    </button> 
  </form>
</template>


<script>
export default {
   data() {
    return {
      title: '',
    }
  },
    methods: {
      onSubmit() {
        this.$emit('addtodo', this.title) 
        if (this.title.length > 30) {
          return
        }
        this.title = ''
      },
  },
}
</script>
