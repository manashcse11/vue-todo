<template>
  <div>
    <h3 class="md-display-3">{{ msg }}</h3>
    <div>
      <md-button class="md-raised">All</md-button>
      <md-button class="md-raised">Incomplete</md-button>
      <md-button class="md-raised">Completed</md-button>
    </div>
    <div>
      <CreateTodo @on-todo="addTodo($event)" />
    </div>
    <md-list>
      <Todo v-for="(todo, index) in todos" :key="index" :description="todo.description" :completed="todo.completed" @on-toggle="toggleTodo(todo)"/>
    </md-list>
  </div>
</template>


<script>
import Todo from './Todo';
import CreateTodo from './CreateTodo';
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
  , methods: {
    addTodo(todo){
      this.todos.push({description: todo, completed: false});
    }
    , toggleTodo(todo){
      todo.completed = !todo.completed;
      console.log(this.todos);
    }
  }
  , components: {
    Todo
    , CreateTodo
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
