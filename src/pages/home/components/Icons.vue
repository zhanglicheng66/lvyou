<template>
    <div class="icons">
      <swiper>
        <swiper-slide v-for="(page,index) in pages" :key='index'>
            <div class="icon" v-for='item in page' :key="item.id">
                <div class="icon-img">
                  <img  class="icon-img-content" :src="item.imgUrl" alt="">
                </div>
                <p class="icon-desc">{{item.desc}}</p>
            </div>

        </swiper-slide>
      </swiper>
    </div>
</template>



<script>
    export default {
        name: "HomeIcons",
        props:{
          list:Array
        },
        components:{

        },
        data (){
          return {
            iconList:[{
              id:'001',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'002',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'003',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'004',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'005',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'006',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票1'
            },{
              id:'007',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'008',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'009',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            },{
              id:'0010',
              imgUrl:'https://gw.alicdn.com/tfs/TB1Wxi2trsrBKNjSZFpXXcXhFXa-183-144.png_.webp',
              desc:'景点门票'
            }]
          }
        },
        methods:{

        },
        computed:{
          pages(){
            const pages =[]
            this.list.forEach((item,index)=>{
              const page = Math.floor(index/8)
                if(!pages[page]){
                  pages[page]=[]
                }
                pages[page].push(item)
            })
            return pages
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
            Updated:function(){

            },
    }
</script>





<style lang='stylus' scoped>
    @import '~@/assets/styles/varibles.styl'
    @import '~@/assets/styles/mixins.styl'

    .icons >>> .swiper-container
        height:0
        padding-bottom:50%
    .icon
        position :relative
        overflow:hidden
        float:left
        width:25%
        height:0
        padding-bottom:25%

        .icon-img
            position :absolute
            top:0
            left:0
            right:0
            bottom:0.44rem
            box-sizing:border-box
            padding:0.1rem
            .icon-img-content
                display :block
                margin:0 auto
                height:100%
        .icon-desc
            position:absolute
            left:0
            right:0
            bottom:0
            height:0.44rem
            line-height:0.44rem
            color:$darkTextColor
            text-align:center
            overflow:hidden
            ellipsis()

</style>
