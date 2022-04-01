<template>
  <div>
    <Back></Back>
    <Navigation></Navigation>
    <Content />
    <router-view></router-view>
  </div>
</template>
<script setup lang="js">
import Navigation from './components/Navigation/index.vue'
import Back from './components/Back.vue'
import Content from './components/Content/index.vue'
export default {
	name: 'App',
  components:{
    Navigation,
    Content,
	  Back
  }
};

</script>

<style lang="scss" >
* {
  cursor: url("./assets/Moony/arrow.cur") 5 5, auto;
  padding: 0;
  margin: 0;
}
//滚动条
</style>

