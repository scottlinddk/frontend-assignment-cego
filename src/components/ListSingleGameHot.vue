<template>
  <span class="games-list__label" v-if="hot === true">HOT</span>
</template>

<script>
export default {
  name: "ListSingleGameHot",
  props: {
    hot: Boolean
  }
}
</script>

<style scoped>
.games-list__label {
  font-weight: 900;
  font-size: 0.8rem;
  padding: 20px 0 0;
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
