<template>
  <div id="app">
    <Header />
    <Main />
    <!-- <Card /> -->

    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
// import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    // Card,
  },
};
</script>

<style lang="scss">
#app {
}
</style>
