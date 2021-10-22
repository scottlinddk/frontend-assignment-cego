<template>
  <span class="games-list__label">HOT</span>
</template>

<script>
export default {
  name: "GameHot"
}
</script>

<style scoped>
.games-list__label {
  font-weight: 900;
  font-size: 1rem;
  padding: 2rem 0 0;
  position: absolute;
  right: -38px;
  text-align: center;
  top: -10px;
  transform: rotate(45deg);
  width: 100px;
  z-index: 10;
  color: #b22222;
  background: gold;
}
</style>
