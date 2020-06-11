<template>
  <div id="app">
    <NavigationBar />
    <ImpressionBanner />
    <ProductFeature />
    <NumberFacts />
    <PricingPlans/>
  </div>
</template>

<script>
import NavigationBar from "./components/NavigationBar.vue";
import ImpressionBanner from "./components/ImpressionBanner.vue";
import ProductFeature from "./components/ProductFeature.vue";
import NumberFacts from "./components/NumberFacts.vue";
import PricingPlans from "./components/PricingPlans.vue";
export default {
  name: "App",
  components: {
    NavigationBar,
    ImpressionBanner,
    ProductFeature,
    NumberFacts,
    PricingPlans
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
