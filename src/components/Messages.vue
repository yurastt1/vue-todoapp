<template>
  <p>
    <span v-if="errorByLength">Максимальна довжина пункту - 30 символів</span><br>
    <span v-if="errorIsAdded">Вже додано</span><br>
    <span v-if="itemDeletedMessage">Успішно видалено</span>
  </p>
</template>

<script>
export default {
  props: ['errorByLength', 'errorIsAdded', 'itemDeletedMessage'],
}
</script>
