<template>
<div class="wrapper">
  <swiper :options="swiperOption" v-if="showSwiper" >
    <swiper-slide v-for="img in list" :key="img.id">
      <img class="swiper-img" :src="img.imgUrl">
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
    export default {
        name: "HomeSwiper",
      props:{
          list:Array
      },
      data (){
          return{
            swiperOption:{
              pagination:".swiper-pagination",
              loop:true,
              autoplay:3000
            },
          }
      },
      computed:{
          showSwiper(){
            return this.list.length;
          }
      }
    }
</script>

<style scoped lang="stylus">
  .wrapper >>> .swiper-pagination-bullet-active{
    background :white !important
  }
  .wrapper{
    width :100%;
    height :0;
    overflow :hidden;
    padding-bottom: 27%;
    background :#eee
  }

  .swiper-img{
    width :100%
  }



</style>
