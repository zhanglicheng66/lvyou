<template>
  <div>
    <transition>
        <slot></slot>
    </transition>
  </div>
</template>



<script>
    export default {
        name: "Fade",
        components:{

        },
        props:{
             
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
  .v-enter, .v-leave-to
    opacity: 0
  .v-enter-active, .v-leave-active
    transition: opacity .5s
</style>
