<template>
  <div class="found">
    <div class="title">发现</div>
    <div class="header">
      <img src="https://fuss10.elemecdn.com/5/2f/94338b99657d5c2a3de1ba17cb660jpeg.jpeg" alt="">
    </div>
    <div class="body">
      <ul class="items">
        <li class="item">
          <p class="text1">百元红包</p>
          <p class="text">兴业银行联名卡</p>
          <img class="img" src="https://fuss10.elemecdn.com/3/cc/a45d2b9d7d09bbc49b40d4e626093jpeg.jpeg" alt="">
        </li>
        <li class="item">
          <p class="text2">金币商城</p>
          <p class="text">0元好物在这里</p>
          <img class="img" src="https://fuss10.elemecdn.com/8/38/9c9aea0e856149083d84af3444b78jpeg.jpeg" alt="">
        </li>
        <li class="item">
          <p class="text3">有红包快抢</p>
          <p class="text">礼包福利领不停</p>
          <img class="img" src="https://fuss10.elemecdn.com/f/85/2bb180f2052c33cfec3852ef2bfccjpeg.jpeg" alt="">
        </li>
        <li class="item">
          <p class="text4">推荐有奖</p>
          <p class="text">5元现金拿不停</p>
          <img class="img" src="https://fuss10.elemecdn.com/6/76/8d42eef97ff4c1c2b671085358541jpeg.jpeg" alt="">
        </li>
        <li class="item">
          <p class="text5">周边优惠</p>
          <p class="text">领取口碑好券</p>
          <img class="img" src="https://fuss10.elemecdn.com/5/10/2351e989d4171479ba0d7b5c06053jpeg.jpeg" alt="">
        </li>
        <li class="item">
          <p class="text6">必吃爆料</p>
          <p class="text">最夯外卖指南</p>
          <img class="img" src="https://fuss10.elemecdn.com/2/36/b784087aff96a97f4e5183d0d784fjpeg.jpeg" alt="">
        </li>
      </ul>
      
    </div>
    <div class="pic">
        <img src="https://fuss10.elemecdn.com/c/1b/cb917876ec34e51ac4a5e24a415a6jpeg.jpeg" alt="">
    </div>
    <div class="footer">
      <p class="title">—— 限时好礼 ——</p>
      <p class="activty">金币换豪礼</p>
      <div class="picture">
        <ul class="items">
          <li class="item">
            <p class="activtyT">限时优惠</p>
            <img src="https://fuss10.elemecdn.com/7/c5/f595b52bc6b50c9899398dccffd42jpeg.jpeg" alt="">
          </li>      
          <li class="item">
            <img src="https://fuss10.elemecdn.com/7/c5/f595b52bc6b50c9899398dccffd42jpeg.jpeg" alt="">
          </li>
          <li class="item">
            <img src="https://fuss10.elemecdn.com/7/c5/f595b52bc6b50c9899398dccffd42jpeg.jpeg" alt="">
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.found {
  height: 100%;
}
.found .title {
  width: 100%;
  height: 30px;
  text-align: center;
  margin-top: 10px;
  line-height: 30px;
}
.found .header {
  border-bottom: 2px solid #cccc;
}
.found .header img {
  width: 100%;
  height: 200px;
}
.body .items {
  margin-left: -25px;
  /* margin-top: 10px; */
}
.body .item {
  list-style-type: none;
  float: left;
  width: 40%;
  height: 70px;
  margin-right: 30px;
  margin-bottom: 0px;
  border-bottom: 1px solid #cccccc;
}
.item .text1 {
  
  color: rgb(232, 143, 40);
}
.item .text2 {
  
  color: rgb(255, 153, 0);
}
.item .text3 {
 
  color: rgb(204, 51, 0);
}
.item .text4 {
  
  color: rgb(27, 169, 225);
}
.item .text5 {
 
  color: rgb(237, 102, 96);
}
.item .text6 {
 
  color: rgb(245, 120, 93);
}
.item .text {
  margin-left: 0px;
  margin-top: -10px;
  font-size: 12px;
  color:#999999;
}
.item .img {
  width: 40px;
  height: 40px;
  margin-left: 100px;
  margin-top: -50px;
  position: absolute;
}
.pic {
  width: 100%;
  height: 200px;
  /* background-color: #ccc; */
  margin-top: 180px;
}
.pic img{
  width: 100%;
  height: 100px;
}
.footer{
  margin-top: -50px;
  margin-left: 100px;
}
.footer .title{
  margin-left: -50px;
  font-weight: 800;
}
.footer .activty {
  font-size: 11px;
  margin-top: -18px;
  margin-left: 48px;
  color: #999;
}
.picture .items {
  margin-left: -130px;
  margin-top: 10px;
}
.picture .item{
  float: left;
  margin-right: 15px;
  height: 200px;
}
.picture .item img {
  width: 100px;
  height: 100px;
}
</style>
