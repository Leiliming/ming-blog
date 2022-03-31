<template>
  <div>
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

<style lang="sass" scoped>
@font-face
  font-family: 'Slideqiuhong'
  src: url('../../assets/fonts/Slideqiuhong-Regular.woff2') format('woff2'),url('../assets/fonts/Slideqiuhong-Regular.woff') format('woff')
  font-weight: normal
  font-style: normal
  font-display: swap

div
  position: relative
  display: flex
  justify-content: space-between
  height: 60px
  padding: 0 200px
  box-sizing: border-box
  // background-color: hsla(0,0%,100%,0.7)
  box-shadow: 0 0 24px 0 rgba(0,0,0,0.1)
  ul
    display: flex
    width: 400px
    justify-content: space-around
    list-style: none
    li
      font-size: 20px
      font-family: 'Slideqiuhong'
      font-weight: normal
      font-style: normal
      line-height: 40px
      width: 50px
      text-align: center
      color: #fff
      margin: 10px 5px
      transition: background .5s linear
      border-radius: 10px
      &:hover
        color: black
        font-size: 20px
        cursor: pointer
        background: #fff
</style> 