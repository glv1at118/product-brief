<template>
  <div id="number-facts">
    <div id="number-facts-img">
      <img src="../assets/about-1.png" alt="img not accessible" />
    </div>
    <div id="number-facts-figures">
      <p class="first-p">{{paragraph1}}</p>
      <p class="second-p">{{paragraph2}}</p>
      <div>
        <section>
          <div class="figure-box">
            <p class="num">653</p>
            <p class="description">Happy Clients</p>
          </div>
        </section>
        <section>
          <div class="figure-box">
            <p class="num">465</p>
            <p class="description">Trusted Users</p>
          </div>
        </section>
        <section>
          <div class="figure-box">
            <p class="num">784</p>
            <p class="description">Projects Done</p>
          </div>
        </section>
        <section>
          <div class="figure-box">
            <p class="num">86</p>
            <p class="description">Conversion Rates</p>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "NumberFacts",
  setup() {
    let paragraph1 = ref("Over 1300+ Completed Projects Still Counting");
    let paragraph2 = ref(
      "dummy text of the printing and typesetting industry. in standard dummy text ever since the"
    );
    return { paragraph1, paragraph2 };
  }
};
</script>

<style lang="scss" scoped>
#number-facts {
  width: 100%;
  margin-top: 100px;
  display: flow-root;
  #number-facts-img {
    width: 50%;
    float: left;

    img {
      width: 100%;
    }
  }
  #number-facts-figures {
    float: left;
    width: 45%;
    margin-left: 5%;

    .first-p {
      margin-top: 30px;
      font-size: 40px;
      width: 100%;
    }
    .second-p {
      margin-top: 30px;
      font-size: 26px;
      width: 100%;
    }
    section {
      width: 50%;
      float: left;

      .figure-box {
        width: 50%;
        height: 30%;
        float: left;
        margin: 50px;
        box-shadow: 0px 5px 15px 1px rgba(#000, 0.2);
        border-radius: 20px;
        border-top-right-radius: 0px;
        text-align: center;
        padding: 30px;

        .num {
          font-size: 38px;
          font-weight: bold;
        }

        .description {
          font-size: 20px;
        }
      }
    }
  }
}
</style>
