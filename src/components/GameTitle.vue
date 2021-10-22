<template>
  <h1 class="game-view__title">{{ title }}</h1>
</template>

<script>
export default {
  name: "GameTitle",
  props: {
    title: String
  }
}
</script>

<style scoped>
.game-view__title {
  margin: 1rem 0 0 0;
}
</style>
