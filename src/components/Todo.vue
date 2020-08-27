<template>
    <md-list-item>{{ description }}</md-list-item>
</template>

<script>
export default {
    name: 'Todo'
    , props: {
        description: String
    }
}
</script>

<style scoped>
</style>