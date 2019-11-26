<template>
  <div class="wapper">
    <swiper :options="swiperOption" v-if="showswiper">
      <swiper-slide v-for="items of list" :key="items.id">
        <img
          class="swiper-img"
          :src="items.imgUrl"
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props:{
    list:Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed:{
   showswiper(){
     return this.list.length
   }
  }
}
</script>
<style scoped lang="stylus">
.wapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 31.25%;

  .swiper-img {
    display: block;
    width: 100%;
    height: 100%;
  }
}
</style>
