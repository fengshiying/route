<template>
  <div>
    <home-header :city="city"></home-header>
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
  import axios from "axios"

  import HomeIcons from "./components/Icons"
    export default {
        name: "Home",
      data(){
          return{
            city:"深圳"

          }
      },
      components:{
        HomeHeader,
        HomeSwiper,
        HomeIcon,
        HomeRecommend,
        HomeWeekend
      },
      methods:{
        getHomeInfo(){
          axios.get("/static/mock/index.json")
            .then(this.getHomeInfoSucc)
        },
        getHomeInfoSucc(res){
          console.log(res);
          res=res.data;
          console.log(res);

        }

      },
      mounted(){
          this.getHomeInfo()

      }
    }
</script>

<style scoped>

</style>
