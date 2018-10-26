<template>
  <div class="header">
   <router-link to="/">
     <div class="iconfont header-icon">&#xe647;</div>
   </router-link>
    城市选择
  </div>

</template>

<script>
    export default {
        name: "CityHeader"
    }
</script>

<style scoped lang="stylus">
  @import "~styles/varibles.styl";
  .header{
    overflow: hidden;
    text-align: center;
    color: #fff;
    height: 100px;
    line-height: 100px;
    background :$bgColor;
    font-size:32px;
  }
  .header-icon{
    top:0;
    left:0;
    position :absolute;
    width :60px;
    font-size:30px;
    text-align :center;
    color: white;
  }

</style>
