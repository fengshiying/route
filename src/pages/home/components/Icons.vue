<template>
  <div class="icons">
    <swiper :options="swiperOption" >
      <swiper-slide v-for="(page,index) in pages"
                    :key="index">
        <div class="icon" v-for="item in page"
             :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl"/>
          </div>
          <p class="icon-dsc">{{item.desc}}</p>
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
      data(){
         return{
     swiperOption:{
       autoplay:false
     }

      }
      },
      computed:{
          pages(){
            const pages=[];
            this.list.forEach((item,index)=>{
              const page=Math.floor(index/8);
              if(!pages[page]){
                pages[page]=[]
              }
              pages[page].push(item)
            })
            return pages;
          }

      }
    }
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl";
  @import "~styles/varibles.styl";
  .icons >>> .swiper-container{
    height: 0;
    padding-bottom:50% ;
  }
  .icon{
    position: relative;
    overflow: hidden;
    float:left;
    height: 0;
    width: 25%;
    padding-bottom: 25%;
  }
  .icon-img{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom:22px;
    box-sizing: border-box;
    padding: 5px;
  }
  .icon-img-content{
    display: block;
    margin: 0 auto;
    height:100%;
  }
  .icon-dsc{
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: 22px;
    line-height: 22px;
    text-align :center;
    color:$darkTextColor;
    overflow :hidden;
    white-space nowrap;
    text-overflow :ellipsis;
      ellipsis();

  }

</style>
