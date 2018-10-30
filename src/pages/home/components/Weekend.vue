<template>
  <div>
    <div class="weekend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in list" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>

      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "HomeWeekend",
    props:{
      list:Array
    }
  }
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl";
  .weekend-title{
    margin-top: 15px;
    height: 65px;
    line-height:65px;
    background: #eee;
    text-indent:30px;
  }
  .item-img-wrapper{
    overflow:hidden;
    height:0;
    padding-bottom:37.09%
  }
  .item-img{
   width: 100%;
  }
  .item-info{
    padding :10px;
  }
  .item-title{
    height: 35px;
    line-height:35px;
    font-size:30px;
    color: #212121;
    ellipsis();
  }
  .item-desc{
    height: 30px;
    line-height: 30px;
    color:#212121;
    margin-top: 20px;
    font-size: 18px;
    padding-bottom :10px;

    ellipsis();
  }



</style>
