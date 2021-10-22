<template>
  <footer>
    <nav id="nav" class="footer__nav">
      <router-link to="/" class="footer__nav-link">View all games</router-link>
    </nav>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
.footer__nav-link {
  font-weight: bold;
  color: #777;
}
.footer__nav-link:hover {
  color: #1181c9;
}
</style>
