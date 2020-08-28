<template>
    <md-list-item @click="$emit('on-toggle')">
        <div :class="{ completed }">{{ description }}</div>
    </md-list-item>    
</template>

<script>
export default {
    name: 'Todo'
    , props: {
        description: String
        , completed: Boolean
    }
}
</script>

<style scoped>
    .completed {
        text-decoration: line-through;
    }
</style>