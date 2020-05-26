<template>
  <div id="app">
    <NavigationBar />
    <ImpressionBanner />
  </div>
</template>

<script>
import NavigationBar from "./components/NavigationBar.vue";
import ImpressionBanner from "./components/ImpressionBanner.vue";
export default {
  name: "App",
  components: {
    NavigationBar,
    ImpressionBanner
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
