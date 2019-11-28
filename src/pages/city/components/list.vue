<template>
    <div class="list" ref="wrapper">
        <div class="">
            <div class="area">
                <div class="little border-topbottom" >您的位置</div>
                <div class="city-choose">
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">热门城市</div>
                <div class="city-choose">
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                    <div class="city-show">
                        <div class="button">北京</div>
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">A</div>
                <div class="name-list">
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">A</div>
                <div class="name-list">
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">A</div>
                <div class="name-list">
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">A</div>
                <div class="name-list">
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">A</div>
                <div class="name-list">
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                </div>
            </div>
            <div class="area">
                <div class="little border-topbottom">A</div>
                <div class="name-list">
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                    <div class="name border-bottom">ale</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import BScroll from 'better-scroll'
export default {
    name:'Citylist',
    mounted (){
        this.scroll=new BScroll(this.$refs.wrapper)
    }
}
</script>
<style lang="stylus" scoped>
    .border-topbottom
        &:before
            border-color #ccc
        &:after
            border-color #ccc
     .border-bottom
        &:before
            border-color #ccc
    .list
        overflow hidden
        position  absolute
        top 1.6rem
        left 0
        right 0
        bottom 0
        .little
            height .4rem
            line-height .4rem
            background #eee
            padding-left .2rem
            font-size .26rem
        .city-choose
            overflow hidden
            padding .1rem .6rem .1rem .1rem
            .city-show
                float left
                width 33.33%
                .button
                    margin .1rem
                    padding .1rem 0
                    text-align center
                    border .02rem solid #ccc
                    border-radius .1rem
        .name-list
            .name
                line-height .6rem
                color #666
                padding-left .2rem
</style>