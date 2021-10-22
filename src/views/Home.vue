<template>
  <main class="home">
    <ListGames></ListGames>
  </main>
</template>

<script>
import ListGames from "../components/ListGames.vue";

export default {
  name: "Home",
  components: {
    ListGames,
  },
};
</script>
