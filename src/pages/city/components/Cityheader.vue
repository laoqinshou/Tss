<template>
    <div class="head">城市选择
        <router-link to='/'>
        <span class="iconfont">&#xe624;</span>
        </router-link>
    </div>
</template>
<script>
export default {
    name:'CityHeader'
}
</script>
<style lang="stylus" scoped>
    .head
        overflow hidden
        height .86rem
        line-height .86rem
        text-align center
        color #fff
        background #00bcd4
        font-size .3rem
        .iconfont
            float left
            margin-left .1rem
            color #fff
</style>