<template>
  <ul class="list">
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
      <li class='item'>A</li>
  </ul>
</template>



<script>
    export default {
        name: "CityAlphabet",
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
    @import '~@/assets/styles/mixins.styl'
    .list
        display :flex
        flex-direction:column
        justify-content :center
        position :absolute
        text-align:center
        right:0
        top:1.58rem
        bottom:0
        width:0.4rem
        .item
            line-height:0.4rem
            text-align:center
            color:$bgColor
</style>
