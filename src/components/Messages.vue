<template>
  <p class="messages">
    <span v-if="errorByLength">Максимальна довжина пункту - 30 символів</span>
    <span v-if="errorIsAdded">Вже додано</span>
    <span v-if="itemDeletedMessage">Успішно видалено</span>
  </p>
</template>

<script>
export default {
  props: ['errorByLength', 'errorIsAdded', 'itemDeletedMessage'],
}
</script>


<style lang="scss">
  .messages {
    background-color: blue;
  }
</style>
