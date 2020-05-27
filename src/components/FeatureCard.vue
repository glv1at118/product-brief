<template>
  <div id="feature-card" v-bind:style="offsetObj">
    <div class="feature-card-core" v-bind:style="positionObj">
      <div class="feature-pic">
        <img src="../assets/icon-1.png" alt="img not accessible" />
      </div>
      <div class="feature-title">{{feature_title}}</div>
      <div class="feature-content">{{feature_content}}</div>
    </div>
  </div>
</template>

<script>
import { ref, onMounted } from "vue";
export default {
  name: "FeatureCard",
  props: [
    "feature_title",
    "feature_content",
    "feature_offset",
    "feature_inner_position"
  ],
  setup(props) {
    let offsetObj = ref({ left: "0px", top: "0px" });
    let positionObj = ref({ "margin-top": "45px" });
    onMounted(() => {
      offsetObj.value.left = props.feature_offset[0];
      offsetObj.value.top = props.feature_offset[1];
      if (props.feature_inner_position === "up") {
        positionObj.value["margin-top"] = "0px";
      } else if (props.feature_inner_position === "down") {
        positionObj.value["margin-top"] = "45px";
      }
    });
    return { offsetObj, positionObj };
  }
};
</script>

<style lang="scss" scoped>
#feature-card {
  width: 360px;
  height: 440px;
  position: absolute;

  .feature-card-core {
    background-color: white;
    width: 100%;
    height: 395px;
    border-radius: 20px;
    box-shadow: 0px 5px 10px 1px rgba(#000, 0.2);
    text-align: center;
    display: flow-root; // change the box into BFC context to contain the margin

    .feature-pic {
      margin-top: 80px;
      margin-bottom: 30px;
    }
    .feature-title {
      font-size: 28px;
      margin-bottom: 30px;
      font-weight: 700;
    }
    .feature-content {
      font-size: 20px;
    }
  }
}
</style>
