<template>
    <div>
        <city-header></city-header>
        <city-search></city-search>
        <city-list></city-list>
        <city-arr></city-arr>
    </div>
</template>
<script>
    import CityHeader from './components/Cityheader'
    import CitySearch from './components/search'
    import CityList from './components/list'
    import CityArr from './components/arraylist'
export default {
    name:'City',
    components:{
        CityHeader,
        CitySearch,
        CityList,
        CityArr
    }
}
</script>
<style lang="stylus" scoped>

</style>