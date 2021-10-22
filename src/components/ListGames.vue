<template>
  <section class="games-list__container">
    <ListSingleGame
      v-for="game in games"
      :key="game.id"
      :id="game.id"
      :title="game.title"
      :hot="game.hot"
      :background="game.background"
      :logo="game.logo"
      :jackpot="game.jackpot"
    >
    </ListSingleGame>
  </section>
</template>

<script>
import games from "../assets/games/games.json";
import ListSingleGame from "./ListSingleGame.vue";

export default {
  name: "ListGames",
  components: {
    ListSingleGame,
  },
  data() {
    return {
      games
    }
  }
}
</script>

<style scoped>
.games-list__container {
  display: grid;
  grid-auto-rows: 14rem;
  grid-template-columns: repeat(1, 1fr);
  gap: 1em;
  margin: 2em;
  padding: 1em 0 1em 0;
}
@media screen and (min-width: 540px) {
  .games-list__container {
    grid-template-columns: repeat(2, 1fr);
    gap: 1em;
    margin: 2em;
    padding: 1em 0 1em 0;
  }
}
@media screen and (min-width: 640px) {
  .games-list__container {
    grid-template-columns: repeat(2, 1fr);
    gap: 1em;
    margin: 2em;
    padding: 1em 0 1em 0;
  }
}
@media screen and (min-width: 768px) {
  .games-list__container {
    grid-template-columns: repeat(3, 1fr);
    gap: 1em;
    margin: 2em;
    padding: 1em 0 1em 0;
  }
}
@media screen and (min-width: 1024px) {
  .games-list__container {
    grid-template-columns: repeat(4, 1fr);
    gap: 1em;
    margin: 2em;
    padding: 1em 0 1em 0;
  }
}
</style>
