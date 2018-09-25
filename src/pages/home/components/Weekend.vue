<template>
  <div>
    <div class="weekend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item in itemList" :key="item.id">
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
    data(){
      return{
        itemList:[
          {
            id:"001",
            imgUrl:"http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg",
            title:"深圳必游TOP10",
            desc:"来到深圳，你需要来这里签到"
          },
          {
            id:"002",
            imgUrl:"http://img1.qunarzz.com/sight/source/1602/88/bf120edeaea383.jpg_r_640x214_f8591f7b.jpg",
            title:"欢乐长隆",
            desc:"世界欢乐汇聚长隆"
          },
          {
            id:"003",
            imgUrl:"http://img1.qunarzz.com/sight/source/1507/d9/2ddc7652fdba16.jpg_r_640x214_5e62f1a3.jpg",
            title:"当地人游深圳",
            desc:"当地人带你发现不一样的深圳"
          },
          {
            id:"004",
            imgUrl:"http://img1.qunarzz.com/sight/source/1505/eb/e4b181a6957c36.jpg_r_640x214_4abbdbc0.jpg",
            title:"情侣好去处",
            desc:"手牵手，一起走到老"
          },
          {
            id:"005",
            imgUrl:"http://img1.qunarzz.com/sight/source/1505/69/e899202f7abddf.jpg_r_640x214_81b6b528.jpg",
            title:"周末亲子游",
            desc:"这个周末就开启美妙的亲子时光"
          }
        ]


      }
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
    padding-bottom:40%
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
