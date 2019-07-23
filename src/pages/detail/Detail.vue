<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content"></div>
  </div>
</template>



<script>

    import DetailBanner from './components/banner'
    import DetailHeader from './components/Header'
    export default {
        name: "Detail",
        components:{
            DetailBanner,
            DetailHeader
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

            }, //用 keepalive会有
            activated (){
              
            }
    
            
    }
</script>





<style  lang='stylus' scoped>
    .content
        height:50rem
</style>
