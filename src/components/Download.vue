<template>
  <div id="download">
    <div class="t">{{title}}</div>
    <div class="d">{{desc}}</div>
    <div class="b">
      <button>{{btn_content}}</button>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Download",
  setup() {
    let title = ref("Download Our Appnox & Grow Your Business");
    let desc = ref("Get Started With A Free 1 Month Trial For Testing");
    let btn_content = ref("Download");
    return { title, desc, btn_content };
  }
};
</script>

<style lang="scss" scoped>
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}

#download {
  background-image: url("../assets/cta-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 500px;
  margin: 80px 0px 80px 0px;
  color: white;
  display: flow-root;

  .t {
    text-align: center;
    font-size: 50px;
    margin: 80px 0px 80px 0px;
  }
  .d {
    text-align: center;
    font-size: 24px;
    margin: 80px 0px 80px 0px;
  }
  .b {
    text-align: center;
    margin: 80px 0px 80px 0px;

    button {
      outline: none;
      border-radius: 30px;
      font-size: 24px;
      font-weight: 700;
      border-style: none;
      border: 2px solid white;
      box-sizing: border-box;
      padding: 12px 30px 12px 30px;
      cursor: pointer;
      @include trans-dura(0.15s);

      &:hover {
        background-color: deeppink;
        color: white;
        border: 2px solid white;
      }
    }
  }
}
</style>
