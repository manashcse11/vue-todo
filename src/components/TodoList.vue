<template>
  <div>
    <h3 class="md-display-3">{{ msg }}</h3>
    <md-list>
      <Todo v-for="(todo, index) in todos" :key="index" :description="todo.description"/>
    </md-list>
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
  .md-list {
    width: 800px;
    max-width: 100%;
    display: inline-block;
    vertical-align: top;
    border: 1px solid rgba(#000, .12);
  }
</style>
