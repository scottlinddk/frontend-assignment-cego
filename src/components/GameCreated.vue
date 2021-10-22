<template>
  <h5 class="game-view-created">Game created: {{ created }}</h5>
</template>

<script>
export default {
  name: "GameCreated",
  props: {
    created: String,
  }
}
</script>

<style scoped>
.game-view-created {
  font-size: 0.6rem;
  font-weight: 200;
  font-style: oblique;
  color: rgb(89, 89, 89);
}
</style>
