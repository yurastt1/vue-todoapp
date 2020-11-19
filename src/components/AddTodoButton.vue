<template>
  <button 
    v-on:click="addTodo"
    type="submit"
    value="Submit"
  >
    add todo
  </button>
</template>


<script>
export default {
  props: ['addTodo'],
}
</script>
