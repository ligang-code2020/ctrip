<template>
  <div id="app">
    <!-- 顶部搜索 -->
    <div class="search-index">
      <div class="search">搜索:目的地/酒店/景点/航班号</div>
      <a href="#" class="user">我 的</a>
    </div>
    <!-- 焦点图模块 -->
    <div class="focus">
      <img src="../src/upload/focus.jpg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style  src="../src/css/ctrip.css"></style>
<style  src="../src/css/normalize.css"></style>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #2c3e50; */
  margin: 0 auto;
}
</style>
