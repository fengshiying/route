<template>
    <div>
      <div class="recommend-title">热门推荐</div>
      <ul>
        <li class="item border-bottom" v-for="item in itemList" :key="item.id">
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
      data(){
          return{
            itemList:[
              {
                id:"001",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1603/9d/9d8c0e9a01bba92e90.water.jpg_200x200_86f2e623.jpg",
                title:"锦绣中华民俗村",
                desc:"锦绣中华.中国民俗文化村是由深圳锦绣中华发展有限公司运营管理的锦绣中华微缩景区和中国民俗文化村两大主题公园.."
              },
              {
                id:"002",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1809/87/8796d4dfe0366858a3.water.png_200x200_ca6e25bf.png",
                title:"世界之窗",
                desc:"世界之窗位于广东省深圳市深圳湾社区深南大道，是中国著名的缩微景区，以弘扬世界文化为宗旨，"
              },
              {
                id:"003",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1502/15/15ca1d0eab6bf46c.water.jpg_200x200_50ca7bb1.jpg",
                title:"东部华侨城大侠谷",
                desc:"大侠谷生态乐园（又名“大峡谷”）位于深圳东部华侨城，俯瞰深圳东部黄金海岸线，集山地郊野公园和都市主题公园"
              },
              {
                id:"004",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_200x200_bc5c0452.jpg",
                title:"深圳小梅沙海洋世界",
                desc:"深圳小梅沙海洋世界坐落在享有“东方夏威夷”美誉的小梅沙海滨，作为国内大规模的海洋主题公园之一，"
             },
              {
                id:"005",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1807/99/992c99c98928c509a3.water.jpg_200x200_fc4df6ea.jpg",
                title:"深圳欢乐谷",
                desc:"深圳欢乐谷是华侨城集团新一代大型主题乐园,首批国家AAAAA级旅游景区,占地面积35万平方米,总投资20亿元人民币,是 一座融参与性、观赏性、娱乐性、"
              },
              {
                id:"006",
                imgUrl:"http://img1.qunarzz.com/sight/p0/201405/30/a9edfcb4fe0e119da480d30d22ade127.jpg_200x200_6af441cf.jpg",
                title:"地王大厦",
                desc:"地王大厦，别名信兴广场。大厦高69层，总高度383.95米（实际建筑高324.8米），建成时曾是亚洲第一高楼"
              },
              {
                id:"007",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1507/e8/2c6ac21e08d919610ee5e7b8b95be052.water.jpg_200x200_704f0dda.jpg",
                title:"大梅沙",
                desc:"大梅沙海滨公园于1999年6月18日建成，建设总投入高达1.2亿元，是广东省5A级旅游景区。位于深圳特区的东部、风光旖旎的大鹏湾畔。这里三面环山"
              }

            ]


          }
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
