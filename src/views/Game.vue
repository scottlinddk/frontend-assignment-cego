<template>
  <div v-if="findCurrentGame(slug)" class="game-view">
    <div class="game-view__content">
      <GameHot v-if="currentGame.hot === true" :hot="currentGame.hot" />
      <GameJackpot :jackpot="currentGame.jackpot" />
      <GameViewBackground
        :background="currentGame.background"
        :title="currentGame.title"
      />
      <GameViewLogo
        :background="currentGame.background"
        :logo="currentGame.logo"
        :title="currentGame.title"
        :height="'200px'"
        :width="'200px'"
      />
    </div>
    <div class="game-view--meta">
      <GameTitle :title="currentGame.title" />
      <GameDesc :description="currentGame.description" />
      <GameTags :tags="currentGame.tags" :id="currentGame.id" />
      <GameCreated :created="currentGame.created" />
    </div>
  </div>
  <div class="game--not-found" v-else>
    <p>
      No game was found. Take a look at
      <router-link class="game__link" to="/">all our games.</router-link>
    </p>
  </div>
</template>

<script>
import games from "../assets/games/games.json";
import GameHot from "../components/GameHot.vue";
import GameJackpot from "../components/GameJackpot.vue";
import GameViewBackground from "../components/GameViewBackground.vue";
import GameViewLogo from "../components/GameViewLogo.vue";
import GameDesc from "../components/GameDesc.vue";
import GameTitle from "../components/GameTitle.vue";
import GameTags from "../components/GameTags.vue";
import GameCreated from "../components/GameCreated.vue";

export default {
  name: "Game",
  components: {
    GameHot,
    GameJackpot,
    GameViewBackground,
    GameViewLogo,
    GameTitle,
    GameDesc,
    GameTags,
    GameCreated,
  },
  data() {
    return {
      games,
      currentGame: {},
      slug: this.$route.params.id,
    };
  },
  methods: {
    findCurrentGame() {
      return (this.currentGame = this.games.find(
        (game) => game.id === this.$route.params.id
      ));
    },
  }
};
</script>
<style>
.game-view {
  position: relative;
  overflow: hidden;
  margin: 3rem auto;
  width: 80%;
  height: 80%;
  border-radius: 0.5rem;
  border: 1px solid rgba(177, 177, 177, 0.255);
  filter: drop-shadow(0 4px 3px rgba(0, 0, 0, 0.07))
    drop-shadow(0 2px 2px rgba(0, 0, 0, 0.06));
}
.game-view__content {
  min-height: 19rem;
  max-height: 19rem;
}
.game-view--meta {
  background: #fff;
  overflow: hidden;
}
.game--not-found {
  margin: 3rem auto;
  padding: 0.5rem 1rem;
  color: #fff;
  border-radius: 1rem;
  width: max-content;
  background: #f87171;
}
.game__link {
  color: #fff;
}
</style>