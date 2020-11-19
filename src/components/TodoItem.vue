<template>
  <li v-on:dblclick="deleteItem">{{ todo.title }}</li>
</template>

<script>
export default {
  props: ['todo', 'deleteItem'],
}
</script>
