<template>
  <p class="game-view__description">{{ description }}</p>
</template>

<script>
export default {
  name: "GameDesc",
  props: {
    description: String
  }
}
</script>

<style scoped>
.game-view__description {
  text-align: left;
  padding: 0 1rem;
}
</style>
