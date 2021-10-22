<template>
  <div class="game-view__jackpot-sign">
    <p class="game-view__jackpot">Jackpot</p>
    <p class="game-view__jackpot-amount">{{ jackpot }}</p>
  </div>
</template>

<script>
export default {
  name: "GameJackpot",
  props: {
    jackpot: String
  }
}
</script>

<style scoped>
.game-view__jackpot-sign {
  background: gold;
  border-radius: 4px;
  display: inline-block;
  line-height: 8px;
  padding: 0.3rem 0.5rem;
  position: absolute;
  left: 0.5rem;
  text-align: center;
  top: 18rem;
  white-space: nowrap;
  z-index: 2;
}
.game-view__jackpot {
  color: #222;
  font-size: 0.7rem;
  font-weight: 900;
  margin: 0 0 0.2rem 0;
  text-transform: uppercase;
}
.game-view__jackpot-amount {
  color: #b22222;
  font-size: 0.8rem;
  font-weight: 900;
  margin: 0;
}
@media screen and (min-width: 540px) {
  .game-view__jackpot-sign {
    top: 17.5rem;
    line-height: 12px;
    padding: 0.5rem 0.7rem;
  }
  .game-view__jackpot {
    font-size: 1rem;
  }
  .game-view__jackpot-amount {
    color: #b22222;
    font-weight: 900;
    margin: 0;
  }
}
</style>
