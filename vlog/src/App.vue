<template>
  <div>
    <Back></Back>
    <Navigation></Navigation>
    <router-view></router-view>
  </div>
</template>
<script setup lang="js">
import Navigation from './components/Navigation/index.vue'
import Back from './components/Back.vue'
export default {
	name: 'App',
  components:{
    Navigation,
	Back
  }
};

</script>

<style lang="sass" >
*
  cursor: url('./assets/Moony/arrow.cur') 5 5 ,auto
  padding: 0
  margin: 0
</style>

