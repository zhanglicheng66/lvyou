<template>
<div>
  <div class="search">
     <input v-model="keyword" type="text" class="search-input" placeholder="输入城市名称或者拼音">
  </div>
  <div class="search-content" ref="search"  v-show="keyword">
      <ul>
        <li class="search-item" v-for="item in list" :key="item.id" border-bottom>
          {{item.name}}
        </li>
        <li class="search-item border-bottom" v-show="hasNoData">
          没有找到数据匹配项
        </li>
      </ul>
  </div>
</div>  
</template>



<script>
    export default {
        name: "CitySearch",
        props:{
          cities:Object
        },
        components:{

        },
        data (){
          return {
            keyword:'',
            list:[],
            timer:null
          }
        },
        methods:{

        },
        computed:{
          hasNoData(){
            return !this.list.length
          }
        },
        watch: {
          keyword(){
            if(this.timer){
              clearTimeout(this.timer)
            }
            if(!this.keyword){
              this.list=[]
              return 
            }
            this.timer = setTimeout(() => {
              const result = []
              for(let i in this.cities){
                this.cities[i].forEach((value)=>{
                  if(value.spell.indexOf(this.keyword)>-1 || value.name.indexOf(this.keyword) > -1){
                    result.push(value)
                  }
                })
              }

              this.list = result
            }, 100);

          }
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
    .search-content
        z-index:10
        overflow :hidden
        position:absolute
        top:1.58rem   
        left:0
        right:0
        bottom:0
        background:#eee
        .search-item
            line-height:0.62rem
            padding-left:0.2rem
            background :#fff
            color:#666     
</style>
