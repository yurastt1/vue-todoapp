<template>
  <div>
    <div class="section">
      <TodoForm 
      @addtodo="addtodo"
      v-bind:todos="todos"
    />
    <Messages 
      v-bind:errorByLength="errorByLength"
      v-bind:errorIsAdded="errorIsAdded"
      v-bind:itemDeletedMessage="itemDeletedMessage"
    />
    </div>

 
    <TodoList 
      v-bind:todos="todos"
      v-bind:deleteItem="deleteItem"
    />
  </div>
</template>

<script>
import TodoForm from './TodoForm'
import TodoList from './TodoList'
import Messages from './Messages'
export default {
   data() {
    return {
      todos: [{id: 1, title: 'mama', completed: true}, {id: 2, title: 'pups', completed: false}],
      errorByLength: false,
      errorIsAdded: false,
      itemDeletedMessage: false,
    }
  },
  components: {
    TodoList,
    TodoForm,
    Messages,
  },
  methods: {
    addtodo(todoTitle) {
      if (todoTitle.length > 30) {
        this.errorByLength = true;
        setTimeout(() =>  this.errorByLength = false, 5000);
        return
      }
      if (this.todos.some(element => element.title === todoTitle)) {
        this.errorIsAdded = true;
        setTimeout(() =>  this.errorIsAdded = false, 5000);
        return
      }
      this.todos.push({id: Date.now(), title: todoTitle});
    },

    deleteItem(item) {
      const deleteItemIndex = this.todos.findIndex(element => element.title === item)
      this.todos.splice(deleteItemIndex, 1);
      this.itemDeletedMessage = true;
      setTimeout(() =>  this.itemDeletedMessage = false, 5000);
    }
  }
}
</script>


