<template>
  <div id="app">
    <router-view />
    <AppFooter v-show="$route.name === 'Game'" />
  </div>
</template>

<script>
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppFooter,
  },
  metaInfo: {
  title: 'CEGO',
  titleTemplate: '%s | Games'
}
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

ul {
  margin: 0;
  padding: 0;
}
</style>
