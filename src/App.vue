<template>
  <div id="app">
    <h1 id="header">Dagbok</h1>
    <Posts />
  </div>
</template>

<script>
import Posts from "./components/Posts.vue";

export default {
  name: "App",
  data() {},

  components: { Posts },
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
#header {
  text-align: center;
}
</style>
