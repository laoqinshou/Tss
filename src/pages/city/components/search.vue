<template>
    <div class="search">
        <input class="search-input" type="text" placeholder="输入城市名或拼音">
    </div>
</template>
<script>
export default {
    name:'CitySearch'
}
</script>
<style lang="stylus" scoped>
    .search
        height .7.2rem
        padding .05rem
        background #00bcd4
        .search-input
            width 100%
            height .62rem
            line-height  .62rem
            text-align center
            border-radius .06rem
</style>