<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>

    <home-icon></home-icon>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>

  </div>

</template>

<script>
  import HomeHeader from "./components/Header"
  import HomeSwiper from "./components/Swiper"
  import HomeIcon from "./components/Icons"
  import HomeRecommend from "./components/Recommend"
  import HomeWeekend from "./components/Weekend"

  import HomeIcons from "./components/Icons"
    export default {
        name: "Home",
      data(){
          return{

          }
      },
      components:{
        HomeHeader,
        HomeSwiper,
        HomeIcon,
        HomeRecommend,
        HomeWeekend
      }
    }
</script>

<style scoped>

</style>
