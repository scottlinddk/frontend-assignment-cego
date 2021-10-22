<template>
  <div>
    <router-link to="/">Game not found. Go back to all games.</router-link>
  </div>
</template>

<script>
export default {
  name: "NotFound",
  metaInfo: {
    title: "CEGO",
    titleTemplate: "%s | Game not found",
  },
};
</script>