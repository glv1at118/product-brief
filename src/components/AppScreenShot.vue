<template>
  <div id="app-screenshot">
    <h1>{{title}}</h1>
    <p>{{intro}}</p>
    <div id="photo-frame">
      <ul>
        <li>
          <img src="../assets/screen-1.jpg" alt="screen shot not accessible" />
        </li>
        <li>
          <img src="../assets/screen-2.jpg" alt="screen shot not accessible" />
        </li>
        <li>
          <img src="../assets/screen-3.jpg" alt="screen shot not accessible" />
        </li>
        <li>
          <img src="../assets/screen-4.jpg" alt="screen shot not accessible" />
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "AppScreenShot",

  setup() {
    let title = ref("App Screenshot");
    let intro = ref(
      "dummy text of the printing and typesetting industry. in standard dummy text ever since"
    );
    return { title, intro };
  }
};
</script>

<style lang="scss" scoped>
@media only screen and (max-width: 800px) {
  #app-screenshot {
    width: 100%;
    position: relative;

    h1,
    p {
      text-align: left !important;
      margin: 50px 0px 50px 0px;
      padding-left: 30px;
    }
    p {
      font-size: 22px;
    }
    #photo-frame {
      width: 290px !important;
      height: 510px;
      position: relative;
      top: 0px;
      left: 50%;
      transform: translateX(-50%);

      ul {
        width: 1160px;
        height: 479px;
        left: 0px !important;
        transform: translateX(0px) !important;
        transform: translateX(-50%);

        li {
          float: left;
          margin: 0px 10px 0px 10px;
          box-shadow: 0px 5px 10px 1px rgba(#000, 0.2);
          cursor: pointer;

          &:hover {
            box-shadow: 0px 5px 10px 8px rgba(#000, 0.2);
          }
        }
      }
    }
  }
}
#app-screenshot {
  width: 100%;
  position: relative;

  h1,
  p {
    text-align: center;
    margin: 50px 0px 50px 0px;
  }
  p {
    font-size: 22px;
  }
  #photo-frame {
    width: 1160px;
    height: 510px;
    position: relative;
    top: 0px;
    left: 50%;
    transform: translateX(-50%);
    overflow-x: scroll;

    ul {
      width: 1160px;
      height: 479px;
      position: relative;
      top: 0;
      left: 50%;
      transform: translateX(-50%);

      li {
        float: left;
        margin: 0px 10px 0px 10px;
        box-shadow: 0px 5px 10px 1px rgba(#000, 0.2);
        cursor: pointer;

        &:hover {
          box-shadow: 0px 5px 10px 8px rgba(#000, 0.2);
        }
      }
    }
  }
}
</style>
