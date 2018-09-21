<template>
<div class="wrapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="img in swiperList" :key="img.id">
      <img class="swiper-img" :src="img.imgUrl">
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
    export default {
        name: "HomeSwiper",
      data (){
          return{
            swiperOption:{
              pagination:".swiper-pagination",
              loop:true
            },
            swiperList:[
              {id:"001",imgUrl:"https://img1.qunarzz.com/qs/1808/c1/96aead8f8ed82902.jpg"},
              {id:"002",imgUrl:"https://img1.qunarzz.com/qs/1809/2b/f060d9035028da02.jpg"},
              {id:"003",imgUrl:"https://img1.qunarzz.com/qs/1808/f1/5237b90429129102.jpg"},
              ]
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
    padding-bottom: 54%;
    background :#eee
  }

  .swiper-img{
    width :100%
  }



</style>
