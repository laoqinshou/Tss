<template>
    <div>
        <div class="c-title">周末去那</div>
        <ul>
            <li class="c-li border-bottom" v-for="item of commlist" :key="item.id">
            <div class="c-img-all">
                <img class="c-img" :src="item.imgurl" alt="">
            </div>
            <div class="c-bottom-title">
                <p class="c-title-acticle">{{item.title}}</p>
                <p class="c-acticle">{{item.desc}}</p>
            </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'week',
  data () {
      return{
          commlist:[{
              id:'1',
              imgurl:'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
              title:'xsfsx',
              desc:'cccccccccccccc'
          },
          {
              id:'2',
              imgurl:'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
              title:'xsfsx',
              desc:'cccccccccccccc'
          },
          {
              id:'3',
              imgurl:'http://img0.imgtn.bdimg.com/it/u=2383721088,3169429672&fm=26&gp=0.jpg',
              title:'xsfsx',
              desc:'cccccccccccccc'
          }
          ]
      }
  }
}
</script>
<style lang="stylus" scoped>
.c-title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
.c-img-all
    overflow hidden
    height 0
    padding-bottom 30%
    .c-img
        width 100%
.c-bottom-title
    padding .1rem
    .c-title-acticle
        line-height .54rem
        font-size .32rem
        verflow hidden;
        white-space nowrap;
        text-overflow ellipsis;
    .c-acticle
        line-height .4rem
        color #ccc
        verflow hidden;
        white-space nowrap;
        text-overflow ellipsis;
</style>
