<template>
  <div class="list" ref="wrapper">
    <div>
        <div class="area">
            <div class="title border-topbottom">当前城市</div>
            <div class="button-list">
                <div class="button-wrapper">
                   <div class="button">{{this.currentCity}}</div>     
                </div>
            </div>
        </div>
        <div class="area">
            <div class="title border-topbottom">热门城市</div>
            <div class="button-list">
                <div 
                class="button-wrapper" 
                v-for="item in hot" 
                :key="item.id"
                @click='handleCityClick(item.name)'    
                >
                    <div class="button">{{item.name}}</div>
                </div>
            </div>
        </div>
        <div class="area" v-for="(item,key) in cities" :key="key" :ref="key">
            <div class="title border-topbottom">{{key}}</div>
            <div class="item-list">
                <div 
                class="item border-bottom" 
                v-for="innerItem in item" 
                :key="innerItem.id"
                 @click='handleCityClick(innerItem.name.name)'
                >{{innerItem.name}}</div>
            </div>
        </div>
    </div>
  </div>
</template>



<script>
    import {mapState,mapMutations} from 'vuex'
    import Bscroll from 'better-scroll'
    export default {
        name: "Citylist",
        props:{
            hot:Array,
            cities:Object,
            letter:String
        },
        components:{
            
        },
        data (){
          return {

          }
        },
        methods:{
            handleCityClick(city){
                this.$store.commit('changeCity',city)
                this.$router.push('/')
            }

        },
        computed:{
            ...mapState({
                currentCity:'city'
            })
        },
        watch: {
            letter(){
                if(this.letter){
                    console.log(this.letter)
                    const element = this.$refs[this.letter][0]
                    this.scroll.scrollToElement(element)
                    console.log(element)

                }
            }
        },
         beforeCreate:function(){

            },
            created:function(){

            },
            beforeMount:function(){

            },
            mounted:function(){
                this.scroll = new Bscroll(this.$refs.wrapper)
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

    .border-topbottom
        &:before
            border-color:#ccc
        &:after
            border-color:#ccc
    .border-bottom
        &:before
            border-color:#ccc   

    .list
        position :absolute
        overflow :hidden 
        top:1.58rem
        left:0
        right:0
        bottom:0 
        .title
            line-height:0.54rem
            background :#eee
            padding-left:0.2rem
            color:#666
            font-size:0.26rem
        .button-list
            overflow :hidden
            padding:0.1rem 0.6rem 0.1rem 0.1rem  
            .button-wrapper
                float:left
                width:33.33%
                .button
                    padding:0.1rem 0
                    margin:0.1rem
                    text-align :center
                    border:0.02rem solid #ccc
                    border-radius:0.06rem

        .item-list
            .item
                line-height :0.76rem
                color:#666
                padding-left:0.2rem
                       


</style>
