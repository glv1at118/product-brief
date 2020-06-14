<template>
  <div id="latest-news">
    <section class="news-title">Latest News</section>
    <section
      class="news-comment"
    >dummy text of the printing and typesetting industry. in standard dummy text ever since the</section>
    <section class="card-box">
      <ul>
        <li v-for="(news, index) in newsContent" v-bind:key="index">
          <div class="news-bkg">
            <img v-bind:src="news.bkgPath" alt="bkg not available" />
            <!-- Vue中和React一样，引入动态img路径需要使用require -->
          </div>
          <div class="btn_box">
            <button>Leadership</button>
            <button>Finance</button>
          </div>
          <div class="title_box">{{news.newsTitle}}</div>
          <div class="info_box">
            <div class="author">By: {{news.newsAuthor}}</div>
            <div class="date">{{news.newsDate}}</div>
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "LatestNews",
  setup() {
    let newsContent = ref([
      {
        newsTitle: "Coding Bridges The Divide It Is The One",
        newsAuthor: "Admin Man",
        newsDate: "15 Dec, 2020",
        bkgPath: require("../assets/blog-1.jpg")
        // 想使用动态img路径则需要使用require
      },
      {
        newsTitle: "Coding Bridges The Divide It Is The One",
        newsAuthor: "Admin Man",
        newsDate: "15 Dec, 2020",
        bkgPath: require("../assets/blog-2.jpg")
      },
      {
        newsTitle: "Coding Bridges The Divide It Is The One",
        newsAuthor: "Admin Man",
        newsDate: "15 Dec, 2020",
        bkgPath: require("../assets/blog-3.jpg")
      }
    ]);
    return { newsContent };
  }
};
</script>

<style lang="scss" scoped>
@mixin trans-dura($duration) {
  transition-timing-function: ease-in-out;
  transition-property: all;
  transition-duration: $duration;
}
#latest-news {
  width: 100%;
  margin-top: 80px;
  box-sizing: border-box;
  padding-top: 50px;
  padding-bottom: 50px;

  .news-title {
    text-align: center;
    font-size: 46px;
    margin-bottom: 30px;
  }
  .news-comment {
    text-align: center;
    font-size: 24px;
    margin-bottom: 30px;
  }
  .card-box {
    width: 80%;
    position: relative;
    left: 10%;
    display: flow-root;
    color: white;

    li {
      float: left;
      width: 30%;
      height: 390px;
      margin-left: 1.66%;
      margin-right: 1.66%;
      box-sizing: border-box;
      padding: 20px;
      overflow: hidden;
      border-radius: 10px;
      box-shadow: 0px 5px 10px 1px rgba(#000, 0.2);
      background-image: url("../assets/blog-2.jpg");
      position: relative;
      @include trans-dura(0.3s);

      &:hover {
        box-shadow: 0px 5px 10px 8px rgba(#000, 0.2);
      }

      &:hover .btn_box,
      &:hover .title_box,
      &:hover .info_box {
        transform: translateY(0px);
      }

      &:hover .title_box,
      &:hover .info_box {
        background-color: rgba(#000, 0.5);
      }

      .news-bkg {
        position: absolute;
        top: 0;
        left: 0;
      }

      .btn_box {
        transform: translateY(-100px);
        @include trans-dura(0.3s);

        button {
          font-size: 16px;
          box-sizing: border-box;
          padding: 5px 10px 5px 10px;
          margin: 0px 30px 0px 0px;
          border-radius: 20px;
          background-color: deeppink;
          color: white;
          outline: none;
          border: 2px solid white;
          cursor: pointer;
          @include trans-dura(0.3s);

          &:hover {
            background-color: black;
          }
        }
      }

      .title_box {
        font-size: 30px;
        margin-top: 200px;
        border-bottom: 1px solid white;
        padding-top: 5px;
        padding-bottom: 5px;
        box-sizing: border-box;
        @include trans-dura(0.3s);
        transform: translateY(58px);
      }
      .info_box {
        display: flow-root;
        padding-top: 5px;
        padding-bottom: 5px;
        @include trans-dura(0.3s);
        transform: translateY(58px);

        .author {
          float: left;
          margin: 0px 30px 0px 0px;
        }
        .date {
          float: left;
        }
      }
    }
  }
}
</style>
