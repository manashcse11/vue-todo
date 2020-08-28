<template>
    <form @submit.prevent="addTodo()">
        <input v-model="todo" type="text" placeholder="Create a new todo...">
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

</style>