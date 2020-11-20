<template>
  <div id="app">
    <TodoApp />
  </div>
</template>

<script>
import TodoApp from './components/TodoApp'
export default {
  name: 'App',
  components: {
    TodoApp
  },
};
</script>


<style lang="scss">
.todo-list {
  margin: 0;
  padding: 0;
  list-style: none;
}

.todo-list li {
  position: relative;
  font-size: 24px;
  border-bottom: 1px solid #ededed;
}

.messages {
  background-color: aqua;
}

</style>
