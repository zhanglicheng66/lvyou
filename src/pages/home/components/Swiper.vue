<template>
  <div class="wrapper">
      <swiper :options="swiperOption">
          <swiper-slide v-for="item in swiperList" :key="item.id">
              <img  class="swiper-img"  :src="item.imgUrl" alt="">
          </swiper-slide>
      </swiper>

      <div class="swiper-pagination" slot="pagination"></div>
  </div>



</template>



<script>
    export default {
        name: "HomeSwiper",
        components:{

        },
        data (){
          return {
              swiperOption:{
                pagination:'.swiper-pagination',
                loop:true
              },
              swiperList:[{
                id:'0001',
                imgUrl:'https://aecpm.alicdn.com/simba/img/TB1CWf9KpXXXXbuXpXXSutbFXXX.jpg_q50.jpg'
              },{
                id:'0002',
                imgUrl:'https://aecpm.alicdn.com/simba/img/TB1CWf9KpXXXXbuXpXXSutbFXXX.jpg_q50.jpg'
              }]
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
            Updated:function(){

            },
    }
</script>





<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background:white !important

.wrapper
    overflow :hidden
    width:100%
    height:0
    padding-bottom:31.25%
    background:#eee
    .swiper-img
        width:100%
</style>
