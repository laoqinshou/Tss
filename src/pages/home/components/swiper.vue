<template>
  <div class="wapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="items of swiperList" :key="items.id">
        <img
          class="swiper-img"
          :src="items.imgurl"
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '1111',
        imgurl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3081108087,555312235&fm=26&gp=0.jpg'
      },
      {
        id: '222',
        imgurl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1392403833,353777295&fm=26&gp=0.jpg'
      },
      {
        id: '333',
        imgurl: 'https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=2939168414,2525881912&fm=26&gp=0.jpg'
      }]
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
