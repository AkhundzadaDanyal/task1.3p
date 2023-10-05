<template>
  <div id="app">
    <MyHeader />
    <router-view />
  </div>
</template>

<script>
import MyHeader from "./components/Header.vue";

export default {
  components: {
    MyHeader,
  },
};
</script>

<style scoped>
/* Reset some default styles for the body */
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji",
    "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; /* Adjust as needed based on your header height */
}

header {
  background-color: #3498db;
  padding: 0px;
  color: white;
}

nav {
  display: flex;
  justify-content: space-around;
  margin-top: 10px;
}

nav a {
  text-decoration: none;
  color: white;
  font-weight: bold;
  font-size: 16px;
}

section {
  margin: 10px;
}
</style>