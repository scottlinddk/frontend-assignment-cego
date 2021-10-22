<template>
  <div class="game-view-tags__container">
    <h4 class="game-view-tags__title">Tags:</h4>
    <ul class="game-view__ul">
      <li v-for="tag in tags" :key="tag.id" class="game-view__tags-item">
        {{ tag }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "GameTags",
  props: {
    tags: Array,
    id: String
  }
}
</script>

<style scoped>
.game-view--tags__container {
  max-width: 90%;
}
.game-view-tags__title {
  margin: 0.5rem 0;
}
.game-view__ul {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  list-style: none;
  padding: 0.5rem;
}
.game-view__tags-item {
  font-size: 0.8rem;
  background: #1181c9;
  color: #fff;
  border-radius: 1rem;
  padding: 0.5rem 1rem;
  margin: 0.2rem;
  transition: transform 1s ease;
  will-change: transform;
}
.game-view__tags-item:hover {
  background: #0c69a3;
  filter: drop-shadow(0 4px 3px rgba(0, 0, 0, 0.07))
    drop-shadow(0 2px 2px rgba(0, 0, 0, 0.06));
  transform: scale(1.1);
}
</style>
