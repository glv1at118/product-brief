<template>
  <div id="faqs">
    <div class="title">Faqs</div>
    <div
      class="desc"
    >dummy text of the printing and typesetting industry. in standard dummy text ever since the</div>
    <div class="content">
      <div class="left">
        <ul>
          <li v-for="(info,index) in infoArr" v-bind:key="index">
            <section class="mark" v-on:click="toggleCard(index)">{{markArr[index]?"hide":"show"}}</section>
            <section class="info1" v-on:click="toggleCard(index)">{{info.info1}}</section>
            <section v-bind:class="['info2', {'info2-inactive': flagArr[index]}]">{{info.info2}}</section>
          </li>
        </ul>
      </div>
      <div class="right">
        <img src="../assets/faqs-1.png" alt="faq img not accessible" />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Faqs",
  setup() {
    let infoArr = ref([
      {
        info1: "How To Buy This?",
        info2:
          "dummy text of the printing and typesetting Lorem has been the industry's standard dummy text ever sinces the 1500s, when an unknown"
      },
      {
        info1: "It Is Refundable?",
        info2:
          "dummy text of the printing and typesetting Lorem has been the industry's standard dummy text ever sinces the 1500s, when an unknown"
      },
      {
        info1: "Can I Use free?",
        info2:
          "dummy text of the printing and typesetting Lorem has been the industry's standard dummy text ever sinces the 1500s, when an unknown"
      },
      {
        info1: "24/7 Supports",
        info2:
          "dummy text of the printing and typesetting Lorem has been the industry's standard dummy text ever sinces the 1500s, when an unknown"
      }
    ]);
    let flagArr = ref([true, true, true, true]);
    let markArr = ref([true, true, true, true]);
    function toggleCard(index) {
      flagArr.value[index] = !flagArr.value[index];
      markArr.value[index] = !markArr.value[index];
    }
    return { infoArr, flagArr, toggleCard, markArr };
  }
};
</script>

<style lang="scss" scoped>
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}

@media only screen and (max-width: 800px) {
  #faqs {
    width: 100%;
    display: flow-root;

    .title {
      text-align: left!important;
      padding-left: 30px;
      font-size: 46px;
      margin: 30px 0px 30px 0px;
    }
    .desc {
      text-align: left!important;
      padding-left: 30px;
      padding-right: 30px;
      font-size: 24px;
      margin: 30px 0px 50px 0px!important;
    }
    .content {
      width: 80%;
      display: flow-root;
      position: relative;
      left: 30px!important;

      .left {
        float: left;
        width: 100%!important;

        li {
          width: 100%;
          padding: 20px;
          box-sizing: border-box;
          box-shadow: 0px 5px 8px 1px rgba(#000, 0.2);
          margin-bottom: 25px;
          border-radius: 10px;
          overflow: hidden;
          position: relative;
          user-select: none;
          @include trans-dura(0.15s);

          &:hover {
            box-shadow: 0px 5px 8px 5px rgba(#000, 0.2);
          }

          .info1 {
            font-size: 28px;
            cursor: pointer;
          }
          .info2 {
            font-size: 20px;
            margin-top: 25px;
          }
          .mark {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 20px;
            font-weight: 700;
            color: gray;
            cursor: pointer;
          }
        }
      }
      .right {
        display: none;
      }
    }
  }
}

#faqs {
  width: 100%;
  display: flow-root;

  .title {
    text-align: center;
    font-size: 46px;
    margin: 30px 0px 30px 0px;
  }
  .desc {
    text-align: center;
    font-size: 24px;
    margin: 30px 0px 100px 0px;
  }
  .content {
    width: 80%;
    display: flow-root;
    position: relative;
    left: 10%;

    .left {
      float: left;
      width: 45%;

      li {
        width: 100%;
        padding: 20px;
        box-sizing: border-box;
        box-shadow: 0px 5px 8px 1px rgba(#000, 0.2);
        margin-bottom: 25px;
        border-radius: 10px;
        overflow: hidden;
        position: relative;
        user-select: none;
        @include trans-dura(0.15s);

        &:hover {
          box-shadow: 0px 5px 8px 5px rgba(#000, 0.2);
        }

        .info1 {
          font-size: 28px;
          cursor: pointer;
        }
        .info2 {
          font-size: 20px;
          margin-top: 25px;
        }
        .mark {
          position: absolute;
          top: 20px;
          right: 20px;
          font-size: 20px;
          font-weight: 700;
          color: gray;
          cursor: pointer;
        }
      }
    }
    .right {
      float: right;
      width: 45%;
    }
    .info2-inactive {
      display: none;
    }
  }
}
</style>
