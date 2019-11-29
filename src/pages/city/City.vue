<template>
    <div>
        <city-header></city-header>
        <city-search></city-search>
        <city-list :hot='hotCities' :listcity='cities'></city-list>
        <city-arr :listcity='cities'></city-arr>
    </div>
</template>
<script>
    import CityHeader from './components/Cityheader'
    import CitySearch from './components/search'
    import CityList from './components/list'
    import CityArr from './components/arraylist'
    import aioxs from 'axios'
export default {
    name:'City',
    components:{
        CityHeader,
        CitySearch,
        CityList,
        CityArr
    },
    data (){
        return{
            cities:{},
            hotCities:[]
        }
    },
    methods :{
        getcitydata(){
            aioxs.get('/api/city.json')
            .then(this.getsucc)
        },
        getsucc(res){
            res=res.data
            if(res.data && res.ret){
                const data = res.data
                this.hotCities = data.hotCities
                this.cities = data.cities
            }
        }
    },
    mounted (){
        this.getcitydata()
    }
}
</script>
<style lang="stylus" scoped>

</style>