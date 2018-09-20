<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe647;</div>

    </div>
    <div class="header-input">
      <span class="iconfont">&#xe611;</span>输入城市景点</div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe64a;</span>
    </div>
  </div>

</template>

<script>
    export default {
        name: "HomeHeader",
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
    width:124px;
    float:right;
    text-align: center;
  }




</style>
