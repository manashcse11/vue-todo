<template>
    <li class="list-group-item">{{ description }}</li>    
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