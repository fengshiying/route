<template>
<div class="wrapper">
  <swiper :options="swiperOption" v-if="showSwiper">
    <swiper-slide v-for="item in list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
    export default {
        name: "HomeSwiper",
      props: {
        list: Array
      },
      data (){
          return{
            swiperOption:{
              pagination: '.swiper-pagination',
              loop: true
            },
            swiperList:[
              {id:"001",imgUrl:"http://img1.qunarzz.com/piao/fusion/1809/86/deb33800de224c02.jpg_750x200_74fb795e.jpg"},
              {id:"002",imgUrl:"http://img1.qunarzz.com/piao/fusion/1805/e8/14b75b1c81fbe702.jpg_750x200_e6d4f1f1.jpg"},
              {id:"003",imgUrl:"http://img1.qunarzz.com/piao/fusion/1809/86/deb33800de224c02.jpg_750x200_74fb795e.jpg"},
              ]
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
    background :white
  }
  .wrapper{
    width :100%;
    height :0;
    overflow :hidden;
    padding-bottom: 26%;
    background :#eee
  }

  .swiper-img{
    width :100%
  }



</style>
