<template>
  <div class="search">
     <input type="text" class="search-input" placeholder="输入城市名称或者拼音">
  </div>
</template>



<script>
    export default {
        name: "CitySearch",
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
    .search
        height:0.72rem
        padding:0 0.1rem
        background :$bgColor
        .search-input
            box-sizing:border-box
            width:100%
            height: 0.62rem
            line-height:0.62rem
            text-align:center
            border-radius:0.6rem
            padding:0 0.1rem
            color:#666
</style>
