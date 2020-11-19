<template>
  <li>{{ todo.title }}</li>
</template>

<script>
export default {
  props: {
    todo: {
      title: String,
      id: Number,
      completed: Boolean,
    }
  },
}
</script>
