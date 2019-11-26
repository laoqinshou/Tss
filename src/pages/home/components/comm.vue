<template>
    <div>
        <div class="c-title">热销推荐</div>
        <ul>
            <li class="c-li border-bottom" v-for="item of list" :key="item.id">
                <img class="c-img" :src="item.imgUrl" alt="">
                <div class="c-bottom-title">
                    <p class="c-title-acticle">{{item.title}}</p>
                    <p class="c-acticle">{{item.desc}}</p>
                    <button class="c-button">详情页面</button>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'comm',
  props:{
    list:Array
 }
}
</script>
<style lang="stylus" scoped>
.c-title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
.c-li
    overflow hidden
    display flex
    height 1.9rem
    .c-img
        width 1.7rem
        height 1.7rem
        padding .1rem
    .c-bottom-title
        flex 1
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
        .c-button
            line-height .44rem
            margin-top .16rem
            background #ff9300
            padding 0 .2rem
            border-radius .06rem
</style>
