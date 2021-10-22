<template>
  <img
    class="game-view__logo"
    :src="logo"
    :alt="'Logo for ' + title"
    :width="width"
    :heigth="height"
  />
</template>

<script>
export default {
  name: "GameViewLogo",
  props: {
    logo: String,
    title: String,
    height: String,
    width: String
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
