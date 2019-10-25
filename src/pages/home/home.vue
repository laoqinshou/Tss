<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-comm></home-comm>
    <home-week></home-week>
  </div>
</template>
<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import HomeComm from './components/comm'
import HomeWeek from './components/weeken'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeComm,
    HomeWeek
  }
}
</script>
<style scoped lang="stylus">

</style>
