<template>
  <div id="navigation-bar">
    <div id="content-box">
      <div id="logo-box">
        <a href="#">
          <img src="../assets/logo-1.png" alt="logo not accessible" />
        </a>
      </div>
      <div id="nav-box">
        <div id="nav-box-left">
          <ul>
            <li v-for="item in navTabNames" v-bind:key="item">
              <a href="#">{{item}}</a>
            </li>
          </ul>
        </div>
        <div id="nav-box-right">
          <div id="purchase-container">
            <button>Purchase</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "NavigationBar",
  setup() {
    const navTabNames = ref(["Home", "Pages", "Services", "Blog", "Contact"]);
    return { navTabNames };
  }
};
</script>

<style lang="scss" scoped>
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}

#navigation-bar {
  background-color: white;
  width: 100%;
  height: 100px;
  box-sizing: border-box;
  box-shadow: 0px 5px 5px 1px rgba(#000, 0.2);
  position: sticky;
  top: 0px;
  left: 0px;
  z-index: 100;

  #content-box {
    height: 100%;
    width: 90%;
    position: absolute;
    left: 5%;

    #logo-box {
      float: left;
      height: 100%;
      width: 15%;
      position: relative;

      a {
        display: block;
        width: 128px;
        height: 48px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }
    }

    #nav-box {
      float: left;
      height: 100%;
      width: 85%;

      #nav-box-left {
        float: left;
        width: 70%;
        height: 100%;
        margin-left: 5%;

        ul {
          width: 100%;
          height: 100%;

          li {
            float: left;
            width: 20%;
            height: 100%;
            line-height: 100px;
            text-align: center;
            font-size: 22px;
            font-weight: 700;

            a {
              @include trans-dura(0.15s);
              color: black;

              &:hover {
                color: red;
              }
            }
          }
        }
      }

      #nav-box-right {
        float: left;
        width: 20%;
        height: 100%;
        position: relative;

        #purchase-container {
          width: 80%;
          height: 60%;
          position: absolute;
          left: 10%;
          top: 20%;

          button {
            width: 100%;
            height: 100%;
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
