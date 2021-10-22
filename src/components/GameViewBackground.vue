<template>
  <div>
    <img
      class="game-view__background"
      :src="background"
      :alt="'Background for ' + title"
      width="100%"
      height="100%"
    />
  </div>
</template>

<script>
export default {
  name: "GameViewBackground",
  props: {
    background: String,
    title: String
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
  color: #fff;
}
.game-view__background {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.game-view__logo {
  margin: 4rem 0;
  -o-object-fit: contain;
  object-fit: contain;
  transition: transform 0.5s ease;
  will-change: transform;
}
.game-view__logo:hover {
  transform: scale(1.2);
}
</style>
