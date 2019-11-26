<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-comm :list="recommendList"></home-comm>
    <home-week :list="weekendList"></home-week>
  </div>
</template>
<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/swiper'
import HomeIcons from './components/icons'
import HomeComm from './components/comm'
import HomeWeek from './components/weeken'
import aioxs from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeComm,
    HomeWeek
  },
  data (){
    return{
      city: '',
      swiperList: [],
      iconList:[],
      recommendList:[],
      weekendList:[]
    }
  },
  methods :{
    //请的具体实现的 步骤要在methods的方法里面写出来
    gethomeinfo(){
      aioxs.get('/api/index.json') //这里是请求的json数据的url地址  一般是放在static里面的  只有放在里面才能访问
      .then(this.gethomesucc)   //这里是一个porimers对  象  返回的是一个this的函数  是在下面的 不用this的话就找不到
    },
    gethomesucc(res){
      //这个方法里面就是成功的数据的显示
      res=res.data
      if(res.ret && res.data){
        const data = res.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted (){
    //这个里面是一个请求的方法    是在页面挂在完成之后的生命周期函数里面
    this.gethomeinfo()
  }
}
</script>
<style scoped lang="stylus">

</style>
