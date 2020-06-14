<template>
  <div id="pricing-plans">
    <div class="upper">
      <h1>Pricing Plans</h1>
      <p>dummy text of the printing and typesetting industry. in standard dummy text ever since the</p>
      <div>
        <button>monthly</button>
      </div>
    </div>
    <div class="lower">
      <div class="card-container">
        <div>
          <section class="part1">PRIMARY</section>
          <section class="part2">
            <img src="../assets/pric-1.png" alt="not accessible" />
          </section>
          <section class="part3">
            <p>Life Time SSL</p>
            <p>1 Dedicated IP</p>
            <p>100 GB storage</p>
            <p>Unlimited Addons</p>
            <p>Windows Server</p>
          </section>
          <section class="part4">
            <button>Get Started</button>
          </section>
        </div>
        <div>
          <section class="part1">POPULAR</section>
          <section class="part2">
            <img src="../assets/pric-2.png" alt="not accessible" />
          </section>
          <section class="part3">
            <p>Life Time SSL</p>
            <p>1 Dedicated IP</p>
            <p>100 GB storage</p>
            <p>Unlimited Addons</p>
          </section>
          <section class="part4">
            <button>Get Started</button>
          </section>
        </div>
        <div>
          <section class="part1">STANDARD</section>
          <section class="part2">
            <img src="../assets/pric-3.png" alt="not accessible" />
          </section>
          <section class="part3">
            <p>Life Time SSL</p>
            <p>1 Dedicated IP</p>
          </section>
          <section class="part4">
            <button>Get Started</button>
          </section>
        </div>
      </div>
    </div>
  </div>
</template>

<script type="javascript">
export default {
  name: "PricingPlans"
};
</script>

<style lang="scss" scoped>
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}

#pricing-plans {
  width: 100%;
  height: 800px;
  margin-top: 150px;
  position: relative;
  background-image: url("../assets/prictable-bg.png");
  background-size: cover;
  background-repeat: no-repeat;

  .upper {
    width: 100%;
    height: 220px;
    text-align: center;

    h1 {
      font-size: 40px;
      margin-bottom: 20px;
    }
    p {
      font-size: 28px;
      margin-bottom: 20px;
    }
    div {
      width: 100%;
      height: 50px;
      text-align: center;
      position: absolute;

      button {
        width: 200px;
        height: 100%;
        border-radius: 25px;
        font-size: 26px;
        outline: none;
        border-style: none;
        border: 2px solid deeppink;
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
  .lower {
    .card-container {
      position: absolute;
      width: 900px;
      height: 500px;
      left: 50%;
      transform: translateX(-50%);

      div {
        padding-bottom: 30px;
        width: 275px;
        float: left;
        margin-left: 12.5px;
        margin-right: 12.5px;
        border-radius: 20px;
        box-shadow: 0px 5px 10px 1px rgba(#000, 0.2);
        background-color: white;

        .part1 {
          text-align: center;
          font-size: 22px;
          margin: 20px 0px 20px 0px;
        }
        .part2 {
          text-align: center;
        }
        .part3 {
          text-align: center;

          p {
            margin: 15px 0px 15px 0px;
          }
        }
        .part4 {
          margin-top: 40px;
          text-align: center;
          button {
            width: 60%;
            height: 40px;
            outline: none;
            border-radius: 30px;
            font-size: 22px;
            font-weight: 700;
            border-style: none;
            border: 2px solid deeppink;
            box-sizing: border-box;
            cursor: pointer;
            @include trans-dura(0.15s);

            &:hover {
              background-color: black;
              color: white;
            }
          }
        }
      }
    }
  }
}
</style>