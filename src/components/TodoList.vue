<template>
  <div>
    <h3 class="md-display-3">{{ msg }}</h3>
    <Todo v-for="(todo, index) in todos" :key="index" :description="todo.description"/>
  </div>
</template>


<script>

import Todo from './Todo';
export default {
  name: 'TodoList',
  props: {
    msg: String
  }
  , data() {
    return {
      todos: [
        { description: "Do the dishes", completed: false },
        { description: "Take out the trash", completed: false },
        { description: "Finish doing laundry", completed: false },
      ],
    };
  }
  , components: {
    Todo
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* .md-card {
      margin-top: 16px;
  } */
</style>
