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
    import {mapState} from 'vuex'
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
              lastCity:'', 
              swiperList:[],
              iconList:[],
              recommendList:[],
              weekendList:[]
          }
        },
        methods:{
          getHomeInfo(){
            axios.get('/api/index.json?city=' + this.city)
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
          ...mapState(['city'])
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
                this.lastCity = this.city
                this.getHomeInfo()

            },
            beforeDestroy:function(){

            },
            destroyed:function(){

            },
            beforeUpdate:function(){

            },
            updated:function(){

            },
            //用 keepalive会有
            activated (){
              if(this.lastCity !== this.city){
                this.lastCity = this.city
                this.getHomeInfo()
              }
            }
    }
</script>





<style scoped>

</style>
