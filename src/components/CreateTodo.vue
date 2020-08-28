<template>
    <form @submit.prevent="addTodo()">
        <md-field md-inline>
            <md-input v-model="todo" type="text" placeholder="Create a new todo..."></md-input>
        </md-field>
    </form>
</template>

<script>
export default {
    name: 'CreateTodo'
    , data() {
        return {
            todo: ""
        };
    }
    , methods: {
        addTodo() {
            if(this.todo.length > 0){
                this.$emit("on-todo", this.todo);
            }
            this.todo = "";
        }
    }
}
</script>

<style scoped>
.md-field{
    width: 800px;
    margin: 0px auto;
}
</style>