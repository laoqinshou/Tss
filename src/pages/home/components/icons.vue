<template>
    <div class="icon">
       <swiper :options="swiperOption">
           
        <div class="child">
            <div class="child-img">
                <img class="imgself" src="http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg" alt="">
            </div>
            <p class="child-font">热门景点</p>
        </div>
         <div class="swiper-pagination" slot="pagination"></div>
       </swiper>
    </div>
</template>
<script>
export default {
  name: 'icons'
}
</script>
<style lang="stylus" scoped>
.icon
    overflow hidden
    width 100%
    height 0
    padding-bottom 50%
    .child
        position relative
        overflow hidden
        float left
        width 25%
        height 0
        padding-bottom 25%
        .child-img
           position absolute
           left 0
           right 0
           top 0
           padding-bottom .4rem
           box-sizing border-box
           padding .1rem
           .imgself
                display block
                margin 0 auto
                width 70%
        .child-font
            position absolute
            left 0
            right 0
            bottom 0
            height .4rem
            line-height .4rem
            text-align center        
</style>
