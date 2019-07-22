<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list='iconList'></home-icons>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
  </div>
</template>



<script>
    import axios from 'axios'
    import HomeHeader from './components/Header'
    import HomeSwiper from './components/Swiper'
    import HomeIcons from './components/Icons'
    import HomeRecommend from './components/Recommend'
    import HomeWeekend from './components/weekend'
    export default {
        name: "Home",
        components:{
          HomeHeader,
          HomeSwiper,
          HomeIcons,
          HomeRecommend,
          HomeWeekend
        },
        data (){
          return {
              city:'上海',
              swiperList:[],
              iconList:[],
              recommendList:[],
              weekendList:[]
          }
        },
        methods:{
          getHomeInfo(){
            axios.get('/api/index.json')
                .then(this.getHomeInfoSucc)
          },
          getHomeInfoSucc(res){
              res=res.data
              if(res.ret&&res.data){
                const data = res.data
                this.swiperList = data.swiperList
                this.iconList = data.iconList
                this.recommendList=data.recommendList
                this.weekendList = data.weekendList
              }
          }

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
            mounted(){
                this.getHomeInfo()

            },
            beforeDestroy:function(){

            },
            destroyed:function(){

            },
            beforeUpdate:function(){

            },
            updated:function(){

            }
    }
</script>





<style scoped>

</style>
