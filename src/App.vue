<template>
  <div id="app">
    <NavigationBar />
    <ImpressionBanner />
    <ProductFeature />
    <NumberFacts />
    <PricingPlans />
    <AppScreenShot />
    <Download />
    <Faqs />
  </div>
</template>

<script>
import NavigationBar from "./components/NavigationBar.vue";
import ImpressionBanner from "./components/ImpressionBanner.vue";
import ProductFeature from "./components/ProductFeature.vue";
import NumberFacts from "./components/NumberFacts.vue";
import PricingPlans from "./components/PricingPlans.vue";
import AppScreenShot from "./components/AppScreenShot.vue";
import Download from "./components/Download.vue";
import Faqs from "./components/Faqs.vue";
export default {
  name: "App",
  components: {
    NavigationBar,
    ImpressionBanner,
    ProductFeature,
    NumberFacts,
    PricingPlans,
    AppScreenShot,
    Download,
    Faqs
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
