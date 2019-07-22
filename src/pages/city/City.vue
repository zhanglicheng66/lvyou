<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alphabet></city-alphabet>
  </div>
</template>



<script>

    import CityHeader from './components/Header'
    import CitySearch from './components/Search'
    import CityList from './components/List'
    import CityAlphabet from './components/Alphabet'
    export default {
        name: "City",
        components:{
            CityHeader,
            CitySearch,
            CityList,
            CityAlphabet
        },
        data (){
          return {

          }
        },
        methods:{

        },
        computed:{

        },
        watch: {

        },
         beforeCreate:function(){

            },
            created:function(){

            },
            beforeMount:function(){

            },
            mounted:function(){

            },
            beforeDestroy:function(){

            },
            destroyed:function(){

            },
            beforeUpdate:function(){

            },
            updated:function(){

            },
    }
</script>





<style scoped>

</style>
