<template>
  <div class="navigation">
    <div></div>
    <ul>
      <li>首页</li>
      <li>技术</li>
      <li>生活</li>
      <li>友链</li>
      <li>留言</li>
      <li>关于</li>
    </ul>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "Navigation"
};
</script>

<style lang="scss" scoped>
@font-face {
  font-family: "Slideqiuhong";
  src: url("../../assets/fonts/Slideqiuhong-Regular.woff2") format("woff2"),
    url("../assets/fonts/Slideqiuhong-Regular.woff") format("woff");
  font-weight: normal;
  font-style: normal;
  font-display: swap;
}

.navigation {
  position: fixed;
  top: 0;
  width: 100vw;
  display: flex;
  justify-content: space-between;
  height: 60px;
  box-sizing: border-box;
  z-index: 999;
  // background-color: hsla(0,0%,100%,0.7)
  // box-shadow: 0 0 24px 0 rgba(0, 0, 0, 0.1);
  ul {
    display: flex;
    width: 400px;
    justify-content: space-around;
    list-style: none;
    li {
      font-size: 20px;
      font-family: "Slideqiuhong";
      font-weight: normal;
      font-style: normal;
      line-height: 40px;
      width: 50px;
      text-align: center;
      color: #fff;
      margin: 10px 5px;
      transition: background 0.5s linear;
      border-radius: 10px;
      &:hover {
        color: black;
        font-size: 20px;
        cursor: pointer;
        background: #fff;
        animation: tada 1s;
      }
    }
  }
}

@keyframes tada {
  from {
    transform: scale3d(1, 1, 1);
  }
  10%,
  20% {
    transform: scale3d(0.9, 0.9, 0.9) rotate3d(0, 0, 1, -3deg);
  }
  30%,
  50%,
  70%,
  90% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, 3deg);
  }
  40%,
  60%,
  80% {
    transform: scale3d(1.1, 1.1, 1.1) rotate3d(0, 0, 1, -3deg);
  }
  to {
    transform: scale3d(1, 1, 1);
  }
}
</style> 