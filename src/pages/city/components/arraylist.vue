<template>
    <div>
        <ul class="list">
            <li  v-for="(item,key) of listcity" :key="key">{{key}}</li>
        </ul>
    </div>
</template>
<script>
export default {
    name:'arrlist',
    props:{
        listcity:Object
    }
    
}
</script>
<style lang="stylus" scoped>
    .list
        display flex
        flex-direction column
        justify-content center
        position absolute
        top 1.5rem
        right 0
        bottom 0
        width .4rem
        li
            text-align center
            color blue
            line-height .4rem
</style>