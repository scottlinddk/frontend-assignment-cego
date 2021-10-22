<template>
  <p class="game-view__description">{{ description }}</p>
</template>

<script>
export default {
  name: "GameFooter",
  props: {
    description: String
  }
}
</script>

<style scoped>
.game-view__description {
  text-align: left;
  padding: 0.5rem 1rem;
}
</style>
