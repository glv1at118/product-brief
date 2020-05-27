<template>
  <div id="impression-banner">
    <div id="phone-box">
      <img src="../assets/hero-mobile-1.png" alt="img not accessible" />
    </div>
    <div id="banner-box">
      <div class="title">{{titleDescription}}</div>
      <div class="content">{{contentDescription}}</div>
      <div class="buttons">
        <button>Get Started</button>
        <button>Learn More</button>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "ImpressionBanner",
  setup() {
    let titleDescription = ref("New Trend Grow Your Business With Appnox App");
    let contentDescription = ref(
      "Lorem ipsum dolor sit amt, consectet adop elit, sed do eius mod ididu There are many"
    );
    return { titleDescription, contentDescription };
  }
};
</script>

<style lang="scss" scoped>
$impression-img-url: "../assets/hero-bg-1.png";
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}

#impression-banner {
  width: 100%;
  height: 800px;
  background-image: url($impression-img-url);
  position: relative;
  overflow: hidden;

  #phone-box {
    position: absolute;
    top: 50%;
    left: 100%;
    transform: translate(-70%, -50%);
  }
  #banner-box {
    width: 40%;
    height: 50%;
    position: absolute;
    top: 25%;
    left: 10%;
    color: white;

    .title {
      font-size: 60px;
      font-weight: 700;
      margin-bottom: 30px;
    }
    .content {
      font-size: 30px;
      margin-bottom: 30px;
    }
    .buttons {
      width: 100%;
      background-color: red;

      button {
        float: left;
        height: 100%;
        outline: none;
        border-radius: 30px;
        font-size: 26px;
        border-style: none;
        border: 2px solid deeppink;
        box-sizing: border-box;
        padding: 12px 30px 12px 30px;
        margin-right: 40px;
        cursor: pointer;
        @include trans-dura(0.15s);

        &:hover {
          background-color: black;
          color: white;
          border: 2px solid white;
        }
      }
    }
  }
}
</style>
