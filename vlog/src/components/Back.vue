<template lang="">
  <div class="header-bg"></div>
  <div class="web-bg"></div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.header-bg {
  width: 100%;
  height: 100vh;
  // cursor: url("../../assetes/s.ico"), default;
  background: url("../assets/bg.jpg") no-repeat center center fixed;
  background-attachment: fixed;
}
.web-bg {
  position: fixed;
  top: 0;
  left: 0;
  z-index: -999;
  width: 100%;
  height: 3000px;
  background: url("https://npm.elemecdn.com/hassan-assets/img/bg_homepage_gray.png");
}
</style>
