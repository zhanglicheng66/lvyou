<template>
  <div class="header">
    城市选择
    <router-link to='/'>
        <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>



<script>
    export default {
        name: "CityHeader",
        components:{

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





<style lang="stylus" scoped>
    @import '~@/assets/styles/varibles.styl'
    .header
        position:relative
        overflow :hidden
        height:0.86rem
        line-height:0.86rem
        text-align:center
        color:#fff
        background:$bgColor
        font-size:0.4rem 
        .header-back
            position:absolute
            width:0.64rem
            text-align:center
            font-size:0.4rem
            top:0
            left:0
            color:#fff

</style>
