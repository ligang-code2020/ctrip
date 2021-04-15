<template>
  <div>
    <!-- 顶部搜索 -->
    <div class="search-index">
      <div class="search">搜索:目的地/酒店/景点/航班号</div>
      <a href="#" class="user">我 的</a>
    </div>
    <!-- 焦点图模块 -->
    <div class="focus">
      <!-- <img src="../src/upload/focus.jpg" alt="" /> -->
      <div class="block">
        <span class="demonstration"></span>
        <el-carousel height="150px" indicator-position="none">
          <el-carousel-item v-for="(item, index) in img_list" :key="index">
            <img :src="item" alt="" />
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
    <!-- 局部导航栏 -->
    <ul class="local-nav">
      <li v-for="(item, index) in local_nav" :key="index">
        <a href="#" :title="item.name">
          <span
            class="local-nav-icon"
            :style="{
              background: 'url(' + item.img + ')',
              backgroundRepeat: 'no-repeat 0 0',
              backgroundSize: '32px auto',
              backgroundPosition: '0 ' + index * -32 + 'px',
            }"
          >
          </span>
          <span>{{ item.name }}</span>
        </a>
      </li>
    </ul>
    <nav>
      <div class="nav-common" v-for="(item, index) in nav" :key="index">
        <div class="nav-items" v-for="(item, index) in item.item" :key="index">{{item.name}}
          <a href="#" v-for="(item, index) in item.center" :key="index" >{{item.text}}
          </a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      img: require("../src/assets/localnav_bg.png"),
      img_list: [
        require("../src/upload/focus.jpg"),
        require("../src/upload/pic3.jpg"),
        require("../src/upload/focus.jpg"),
      ],
      style: "",
      local_nav: [
        {
          name: "景点游玩",
          img: require("../src/assets/localnav_bg.png"),
        },
        {
          name: "周边游",
          img: require("../src/assets/localnav_bg.png"),
        },
        {
          name: "美食林",
          img: require("../src/assets/localnav_bg.png"),
        },
        {
          name: "一日游",
          img: require("../src/assets/localnav_bg.png"),
        },
        {
          name: "当地攻略",
          img: require("../src/assets/localnav_bg.png"),
        },
      ],
      nav: [
        {
          item: [
            {
               name:"12"
            },
            {
              center: [
                {
                  text: "海外酒店"
                },
                {
                  text: "特价酒店"
                },
              ],
            },
            {
              center: [{text: "海外酒店"}, {text: "海外酒店"}],
            },
          ],
        },
        {
          item: [
            {
              name:"1"
            },
            {
              center: [{}, {}],
            },
            {
              center: [{}, {}],
            },
          ],
        },
        {
          item: [
            {
              name:"1"
            },
            {
              center: [{}, {}],
            },
            {
              center: [{}, {}],
            },
          ],
        },
      ],
    };
  },
  mounted() {
    // this.style = {
    //           background: 'url(' + this.img + ')',
    //           backgroundRepeat: 'no-repeat 0 0',
    //           backgroundSize: 32px+ auto',
    //         }
  },
};
</script>

<style src="../src/css/ctrip.css"></style>
<style src="../src/css/normalize.css"></style>
<style>
/* body{
  margin: 0 auto;
} */

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 0;
  margin: 0;
}
.el-carousel__arrow--right {
  display: none;
}
.el-carousel__arrow--left {
  display: none;
}
</style>
