<template>
    <md-card class="md-primary" md-theme="purple-card" md-with-hover>
      <md-ripple>
        <md-card-header>
          <div class="md-title">{{ description }}</div>
        </md-card-header>
      </md-ripple>
    </md-card>
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
    .md-card {
      margin-top: 16px;
    }
</style>