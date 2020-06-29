<template>
  <div id="product-feature" v-on:resize="resizeHook">
    <div class="feature-card card1">
      <div class="feature-card-core">
        <div class="feature-pic">
          <img src="../assets/icon-1.png" alt="img not accessible" />
        </div>
        <div class="feature-title">Easy Customize</div>
        <div
          class="feature-content"
        >mext of the printing and has been typesetting industry. Lorem bee the industry's standard</div>
      </div>
    </div>
    <div class="feature-card card2">
      <div class="feature-card-core">
        <div class="feature-pic">
          <img src="../assets/icon-1.png" alt="img not accessible" />
        </div>
        <div class="feature-title">Responsive Ready</div>
        <div
          class="feature-content"
        >mext of the printing and has been typesetting industry. Lorem bee the industry's standard</div>
      </div>
    </div>
    <div class="feature-card card3">
      <div class="feature-card-core">
        <div class="feature-pic">
          <img src="../assets/icon-1.png" alt="img not accessible" />
        </div>
        <div class="feature-title">Cloud Storage</div>
        <div
          class="feature-content"
        >mext of the printing and has been typesetting industry. Lorem bee the industry's standard</div>
      </div>
    </div>
  </div>
</template>

<script>
// import { ref, onMounted } from "vue";
export default {
  name: "ProductFeature",
  setup() {
    return {};
  }
};
</script>

<style lang="scss" scoped>
#product-feature {
  width: 100%;
  height: 540px;
  position: relative;

  .feature-card {
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

  .card1 {
    top: 80px;
    left: 200px;
    margin-top: 45px;
  }
  .card2 {
    top: 80px;
    left: 600px;
    margin-top: 0px;
  }
  .card3 {
    top: 80px;
    left: 1000px;
    margin-top: 45px;
  }
}

@media only screen and (max-width: 800px) {
  #product-feature {
    width: 100%;
    height: 1320px;
    position: relative;
    display: flow-root!important;

    .feature-card {
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

    .card1 {
      top: 0px;
      left: 50%;
      transform: translateX(-50%);
    }
    .card2 {
      top: 460px;
      left: 50%;
      transform: translateX(-50%);
    }
    .card3 {
      top: 830px;
      left: 50%;
      transform: translateX(-50%);
    }
  }
}
</style>
