<template>
  <div>
    <div class="item" v-for="(item,index) in list" :key="index">
        <div class="item-title border-bottom">
            <span class="item-title-icon"></span>
            {{item.title}}
        </div>
        <div v-if="item.children" class="item-chilren">
            <detail-list1 :list="item.children"></detail-list1>
        </div>
    </div>
  </div>
</template>



<script> 
    export default {
        name: "DetailList1",
        props:{
            list:Array
        },
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

            }, //用 keepalive会有
            activated (){
              
            },
            deactivated(){
              
            }
    
            
    }
</script>





<style lang="stylus" scoped>
  .item-title-icon
    position: relative
    left: .06rem
    top: .06rem
    display: inline-block
    width: .36rem
    height: .36rem
    background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
    margin-right: .1rem
    background-size: .4rem 3rem
  .item-title
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
  .item-chilren
    padding: 0 .2rem
</style>
