<template>
    <div>
      <div class="recommend-title">热门推荐</div>
      <ul>
        <li class="item border-bottom" v-for="item in list" :key="item.id">
            <img class="item-img" :src="item.imgUrl"/>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>

        </li>
      </ul>
    </div>
</template>

<script>
    export default {
        name: "Recommend",
      props:{
          list:Array
      }
    }
</script>

<style scoped lang="stylus">
  @import "~styles/mixins.styl";
  .recommend-title{

    margin-top: 15px;
    height: 45px;
    line-height: 45px;
    background: #eee;
    text-indent:30px;
  }
  .item{
    display: flex;
    height:200px;
    overflow: hidden;
  }
  .item-img{
    display: block;
    width:200px;
    height: 200px;
    padding:10px;
  }
  .item-info{
    margin-top: 20px;
    flex: 1;
    padding: 10px;
    min-width 0;
  }
  .item-title{
    height: 32px;
    line-height:32px;
    font-size:30px;
    color: #212121;
    ellipsis()
  }
  .item-desc{
    height: 20px;
    line-height: 20px;
    color:#212121;
    margin-top: 10px;
    font-size: 18px;
    ellipsis()
  }
  .item-button{
    background:#ffab1e;
    padding: 10px;
    border-radius: 5px;
    margin-top: 10px;
    text-overflow: ellipsis;
    font-size: 20px;
    color:#fff;
  }


</style>
