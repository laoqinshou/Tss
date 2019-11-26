<template>
  <div class="header">
      <div class="header-left">
        <span class="iconfont">&#xe624;</span>
      </div>
      <div class="header-input">
        城市/搜索/内容
        <span class="iconfont"></span>
      </div>
      <div class="header-right">
        {{this.city}}
        <span class="iconfont"> &#xe6aa;</span>
      </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeaders',
  props:{
    city:String
  }
}
</script>
<style scoped lang='stylus'>
@import '../../../assets/styles/varibles.styl'
  .header
    display flex
    height .86rem
    background $bgcolor
    color #fff
    .header-left
        width .64rem
        margin-top  .2rem
        text-align: center
    .header-input
        flex 1
        height .64rem
        line-height .64rem
        margin-top .12rem
        margin-left .2rem
        background #fff
        border-radius .1rem
        padding-left .2rem
        color #ccc
    .header-right
        width 1.24rem
        margin-top .2rem
        text-align: center
</style>
