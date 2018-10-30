<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe647;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe611;</span>输入城市景点</div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont">&#xe64a;</span>
      </div>
    </router-link>

  </div>

</template>

<script>
    export default {
        name: "HomeHeader",
      props:{
          city:String
      },
      data(){
          return{
          }
      }
    }
</script>

<style scoped lang="stylus">
  @import "~styles/varibles.styl";
  .header{
    display:flex;
    line-height: 86px ;
    background :$bgColor;
    color: #fff;
  }

  .header-left{
    width:64px;
    float:left;
  }
  .back-icon{
    text-align:center;
    font-size:20px;
  }
  .header-input{
    flex: 1;
    height: 64px;
    margin-top:10px;
    margin-left: 20px;
    background: #fff;
    border-radius: 10px;
    color:#ccc;
    line-height: 64px;
    padding-left: 10px;
    }
  .header-right{
    width:104px;
    padding :10px;
    float:right;
    color :white;
    text-align: center;
  }




</style>
