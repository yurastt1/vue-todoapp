<template>
  <button 
    v-on:click="addTodo"
  >
    add todo
  </button>
</template>


<script>
export default {
  props: ['addTodo'],
}
</script>
