<template>
  <input
    v-bind:title="title"
    v-on:input="$emit('input', $event.target.value)"
  >
</template>

<script>
export default {
  props: ['title']
}
</script>
