<template>
  <article class="games-list__item">
    <router-link :to="'/game/' + id">
      <div class="games-list__content">
        <ListSingleGameHot :hot="hot" />
        <GameViewBackground :background="background" />
        <GameViewLogo
          class="games-list__logo"
          :logo="logo"
          :height="'100px'"
          :width="'100px'"
        />
      </div>
      <ListSingleGameFooter :jackpot="jackpot" />
    </router-link>
  </article>
</template>

<script>
import GameViewBackground from "@/components/GameViewBackground.vue";
import GameViewLogo from "@/components/GameViewLogo.vue";
import ListSingleGameHot from "@/components/ListSingleGameHot.vue";
import ListSingleGameFooter from "@/components/ListSingleGameFooter.vue";

export default {
  name: "ListSingleGame",
  props: {
    id: String,
    title: String,
    hot: Boolean,
    background: String,
    logo: String,
    jackpot: String
  },
  components: {
    GameViewBackground,
    GameViewLogo,
    ListSingleGameHot,
    ListSingleGameFooter
  }
}
</script>

<style scoped>
.games-list__item {
  width: 100%;
  cursor: pointer;
  overflow: hidden;
  border-radius: 0.5rem;
  border: 1px solid rgba(177, 177, 177, 0.255);
  filter: drop-shadow(0 4px 3px rgba(0, 0, 0, 0.07))
    drop-shadow(0 2px 2px rgba(0, 0, 0, 0.06));
}
.games-list__content {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
  height: 100%;
  width: 100%;
}
.games-list__logo {
  margin: 0 0 2.5rem 0;
}
</style>
