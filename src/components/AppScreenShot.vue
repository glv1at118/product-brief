<template>
  <div id="app-screenshot">
    <h1>{{title}}</h1>
    <p>{{intro}}</p>
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
</style>
