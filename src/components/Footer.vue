<template>
  <div id="footer">
    <div class="upper">
      <section class="column-1">
        <div>Quick Link</div>
        <p>
          <a href="#">Help Center</a>
        </p>
        <p>
          <a href="#">Privacy Policy</a>
        </p>
        <p>
          <a href="#">Supports</a>
        </p>
        <p>
          <a href="#">Terms & Conditions</a>
        </p>
        <p>
          <a href="#">About Us</a>
        </p>
        <p>
          <a href="#">Contact</a>
        </p>
      </section>
      <section class="column-2">
        <div>Quick Link</div>
        <p>
          <a href="#">Help Center</a>
        </p>
        <p>
          <a href="#">Privacy Policy</a>
        </p>
        <p>
          <a href="#">Supports</a>
        </p>
        <p>
          <a href="#">Terms & Conditions</a>
        </p>
        <p>
          <a href="#">About Us</a>
        </p>
        <p>
          <a href="#">Contact</a>
        </p>
      </section>
      <section class="column-3">
        <div>Quick Link</div>
        <p>
          <a href="#">Help Center</a>
        </p>
        <p>
          <a href="#">Privacy Policy</a>
        </p>
        <p>
          <a href="#">Supports</a>
        </p>
        <p>
          <a href="#">Terms & Conditions</a>
        </p>
        <p>
          <a href="#">About Us</a>
        </p>
        <p>
          <a href="#">Contact</a>
        </p>
      </section>
      <section class="column-4">
        <div>Quick Link</div>
        <p>
          <a href="#">Help Center</a>
        </p>
        <p>
          <a href="#">Privacy Policy</a>
        </p>
        <p>
          <a href="#">Supports</a>
        </p>
        <p>
          <a href="#">Terms & Conditions</a>
        </p>
        <p>
          <a href="#">About Us</a>
        </p>
        <p>
          <a href="#">Contact</a>
        </p>
      </section>
    </div>
    <div class="lower">© 2020 All Right Reserved by theme_group</div>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style lang="scss" scoped>
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}

@media only screen and (max-width: 500px) {
  #footer {
    width: 100%;
    height: 600px;
    margin-top: 50px;
    background-image: url("../assets/foot-bg.png");
    background-repeat: no-repeat;
    background-position: 0px -100px;
    border-top: 1px solid lightgray;
    position: relative;

    .upper {
      width: 80%;
      height: 430px;
      margin-top: 60px;
      position: relative;
      top: 0px;
      left: 10%;

      .column-1,
      .column-2,
      .column-3,
      .column-4 {
        width: 25%;
        float: left;
        box-sizing: border-box;
        padding-left: 30px;

        div {
          font-size: 20px !important;
          color: white;
          font-weight: 700;
          margin: 20px 0px 20px 0px;
        }

        p {
          font-size: 14px !important;
          margin: 15px 0px 15px 0px;

          a {
            color: white;

            &:hover {
              color: red;
            }
          }
        }
      }
    }
    .lower {
      width: 80%;
      height: 60px;
      line-height: 60px;
      color: white;
      position: absolute;
      bottom: 50px;
      left: 10%;
      text-align: center;
      font-size: 20px;
      box-sizing: border-box;
      border-top: 1px solid white;
    }
  }
}

#footer {
  width: 100%;
  height: 600px;
  margin-top: 50px;
  background-image: url("../assets/foot-bg.png");
  background-repeat: no-repeat;
  background-position: 0px -100px;
  border-top: 1px solid lightgray;
  position: relative;

  .upper {
    width: 80%;
    height: 430px;
    margin-top: 60px;
    position: relative;
    top: 0px;
    left: 10%;

    .column-1,
    .column-2,
    .column-3,
    .column-4 {
      width: 25%;
      float: left;
      box-sizing: border-box;
      padding-left: 30px;

      div {
        font-size: 28px;
        color: white;
        font-weight: 700;
        margin: 20px 0px 20px 0px;
        @include trans-dura(0.3s);
      }

      p {
        font-size: 18px;
        margin: 15px 0px 15px 0px;
        @include trans-dura(0.3s);

        a {
          color: white;

          &:hover {
            color: red;
          }
        }
      }
    }
  }
  .lower {
    width: 80%;
    height: 60px;
    line-height: 60px;
    color: white;
    position: absolute;
    bottom: 50px;
    left: 10%;
    text-align: center;
    font-size: 20px;
    box-sizing: border-box;
    border-top: 1px solid white;
  }
}
</style>
