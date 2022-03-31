<template lang="">
    <div class="video-bg">
        <video width="320" height="240" autoplay loop muted>
         <!-- <source src="https://assets.codepen.io/3364143/7btrrd.mp4" type="video/mp4"> -->
         <source src="../assets/video1.mp4" javascript="video" type="video/mp4">
       Your browser does not support the video tag.
       </video>
    </div>
</template>
<script>

export default {};
</script>
<style lang="sass" scoped>
.video-bg
  position: fixed
  right: 0
  top: 0
  width: 100vw
  height: 100vh
  cursor: url('../assetes/s.ico'), default
  video
    width: 100%
    height: 100%
    object-fit: cover
</style>