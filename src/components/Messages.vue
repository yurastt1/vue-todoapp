<template>
  <div>
    <span v-if="errorByLength">Максимальна довжина пункту - 30 символів</span>
    <span v-if="errorIsAdded">Вже додано</span>
    <span v-if="itemDeletedMessage">Успішно видалено</span>
  </div>
</template>

<script>
export default {
  props: ['errorByLength', 'errorIsAdded', 'itemDeletedMessage']
}
</script>
