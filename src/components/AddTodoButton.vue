<template>
  <button 
    type="submit"
    value="Submit"
    v-bind="title"
    :disabled="!!title"
  >
     add task
  </button>
</template>

<script>
export default {
  props: ['title']
}
</script>


