<template>
  <div id="product-feature">
    <FeatureCard
      v-bind:feature_offset="['200px','80px']"
      feature_title="Easy Customize"
      feature_content="mext of the printing and has been typesetting industry. Lorem bee the industry's standard"
      feature_inner_position="down"
    />
    <FeatureCard
      v-bind:feature_offset="['600px','80px']"
      feature_title="Responsive Ready"
      feature_content="mext of the printing and has been typesetting industry. Lorem bee the industry's standard"
      feature_inner_position="up"
    />
    <FeatureCard
      v-bind:feature_offset="['1000px','80px']"
      feature_title="Cloud Storage"
      feature_content="mext of the printing and has been typesetting industry. Lorem bee the industry's standard"
      feature_inner_position="down"
    />
  </div>
</template>

<script>
// import { ref } from "vue";
import FeatureCard from "./FeatureCard.vue";
export default {
  name: "ProductFeature",
  setup() {
    return {};
  },
  components: {
    FeatureCard
  }
};
</script>

<style lang="scss" scoped>
#product-feature {
  width: 100%;
  height: 540px;
  position: relative;
}
</style>
