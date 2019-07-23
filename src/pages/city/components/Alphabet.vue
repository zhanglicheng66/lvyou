<template>
  <ul class="list">
      <li 
      class='item' 
      v-for='item in letters' 
      :key="item"
      :ref="item"
      @touchstart = "handleTouchStart"
      @touchmove = "handleTouchMove"
      @touchEnd = "handleTouchEnd"
      @click= "handleLetterClick"
      >{{item}}</li>
  </ul>
</template>



<script>
    export default {
        name: "CityAlphabet",
        props:{
          city:Object
        },
        components:{
            
        },
        data (){
          return {
            touchStatus:false,
            startY:0,
            timer:null
          }
        },
        methods:{
          handleLetterClick(e){
            this.$emit('change',e.target.innerText)
          },
          handleTouchStart(){
            this.touchStatus = true 
          },
          handleTouchMove(e){
            if(this.touchStatus){
              if(this.timer){
                clearTimeout(this.timer)
              }
              this.timer = setTimeout(() => {
                  const touchY = e.touches[0].clientY - 79
                  const index = Math.floor((touchY - this.startY)/20)
                  if(index>=0 && index < this.letters.length){
                    this.$emit('change',this.letters[index])
                  }
              }, 15);
            }
          },
          handleTouchEnd(){
            this.touchStatus = false
          }
        },
        computed:{
          letters(){
              const letters = []
              for (let i in this.city){
                letters.push(i)
              }
              return letters
            }
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
                this.startY = this.$refs['A'][0].offsetTop
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
