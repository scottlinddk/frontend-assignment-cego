<template>
  <footer class="games-list__description">
    <p class="games-list__title">Jackpot:</p>
    <p class="games-list__jackpot">{{ jackpot }}</p>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="games-list__cta"
      viewBox="0 0 20 20"
      fill="green"
    >
      <path
        fill-rule="evenodd"
        d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z"
        clip-rule="evenodd"
      />
    </svg>
  </footer>
</template>

<script>
export default {
  name: "ListSingleGameFooter",
  props: {
    jackpot: String
  }
}
</script>

<style scoped>
.games-list__description {
  position: absolute;
  text-align: left;
  bottom: 0;
  width: 100%;
  background-color: #fff;
  display: grid;
  grid-template:
    "title . . cta"
    "jackpot . . cta";
  height: 3rem;
  padding: 0;
}
.games-list__title {
  grid-area: title;
  font-weight: 500;
  font-size: 0.6rem;
  color: black;
  margin: 0.4rem 0 0 0.4rem;
  padding: 0;
}
.games-list__jackpot {
  grid-area: jackpot;
  font-weight: 900;
  color: #70a7c2;
  margin: 0 0 0.5rem 0.4rem;
  padding: 0;
}
.games-list__cta {
  grid-area: cta;
  place-self: center;
  height: 2rem;
  width: auto;
  color: green;
  margin: 0;
  transition: transform 0.5s ease;
  will-change: transform;
}
.games-list__cta:hover {
  transform: scale(1.2);
  filter: drop-shadow(0 4px 3px rgba(208, 208, 208, 0.555));
}
</style>
