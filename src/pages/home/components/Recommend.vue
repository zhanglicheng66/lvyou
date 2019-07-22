<template>
  <div>
     <div class="title">热销推荐</div>
     <ul>
       <li class="item border-bottom" v-for="item in list" :key="item.id">
         <img class="item-img" :src="item.imgUrl" alt="图片">
         <div class="item-info">
           <p class="item-title">{{item.title}}</p>
           <p class="item-desc">{{item.desc}}</p>
           <button class="item-button">查看详情</button>
         </div>
       </li>
     </ul>
  </div>
</template>



<script>
    export default {
        name: "HomeRecommend",
        props:{
          list:Array
        },
        components:{

        },
        data (){
          return {
            recommendList:[{
              id:'001',
              img:'https://imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
              title:'日本樱花季',
              desc:'魅力的日本樱花季节漫天飞舞 飞田新地'
            },
            {
              id:'002',
              img:'https://imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
              title:'日本樱花季',
              desc:'魅力的日本樱花季节漫天飞舞 飞田新地'
            },
            {
              id:'003',
              img:'https://imgs.qunarzz.com/p/p29/201302/28/3d20251a1b60350a93835fbb.jpg_256x160_e8f468b0.jpg',
              title:'日本樱花季',
              desc:'魅力的日本樱花季节漫天飞舞 飞田新地'
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





<style lang="stylus" scoped>
    @import '~@/assets/styles/mixins.styl'
    .title
        margin-top:0.2rem
        line-height :0.8rem
        background :#eee
        text-indent:0.2rem
    .item
        overflow :hidden
        display :flex
        height 1.9rem
        .item-img
            width:1.7rem
            height:1.7rem
            padding:0.1rem
        .item-info
            flex:1
            padding:0.1rem
            min-width:0
            .item-title
                  line-height:0.54rem
                  font-size:0.32rem
                  ellipsis()
            .item-desc
                  line-height :0.4rem
                  color:'black'
                  ellipsis()
            .item-button
                  line-height:0.44rem
                  margin-top:0.2rem
                  background :#ff9300
                  padding:0 0.2rem
                  border-radius:0.86rem
                  color:#fff
</style>
