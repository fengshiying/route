<template>
<div class="wrapper">
  <swiper :options="swiperOption" >
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
              {id:"001",imgUrl:"http://img1.qunarzz.com/piao/fusion/1805/e8/14b75b1c81fbe702.jpg_750x200_e6d4f1f1.jpg"},
              {id:"002",imgUrl:"http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg"},
              {id:"003",imgUrl:"http://img1.qunarzz.com/piao/fusion/1808/3e/f1975f6bde70b202.jpg_750x200_c28601f0.jpg"},
              {id:"004",imgUrl:"http://img1.qunarzz.com/piao/fusion/1809/86/deb33800de224c02.jpg_750x200_74fb795e.jpg"},
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
    padding-bottom: 27%;
    background :#eee
  }

  .swiper-img{
    width :100%
  }



</style>
