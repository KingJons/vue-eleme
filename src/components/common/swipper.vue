<template>
  <div class="swipper">
      <mt-swipe :auto="0">
        <mt-swipe-item>
            <ul class="items">
                <li class="item">
                    <i class="icon iconfont" style="color: #FFC125">&#xe64a;</i>
                    <span>美食</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FFD700">&#xe62c;</i>
                    <span>早餐</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #87CEFA">&#xe635;</i>
                    <span>便利</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FFF000">&#xe63a;</i>
                    <span>果蔬</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #87CEEB">&#xe774;</i>
                    <span>特惠</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #F4A460">&#xe741;</i>
                    <span>简餐</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FF3030">&#xe601;</i>
                    <span>红包</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #CAE1FF">&#xe624;</i>
                    <span>健康</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FFFF00">&#xe607;</i>
                    <span>甜品</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FA8072">&#xe600;</i>
                    <span>鲜花</span></li>
            </ul>
        </mt-swipe-item>
        <mt-swipe-item>
            <ul class="items">
                <li class="item">
                    <i class="icon iconfont" style="color: #FFC125">&#xe64a;</i>
                    <span>披萨</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FFD700">&#xe75d;</i>
                    <span>便当</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #87CEFA">&#xe742;</i>
                    <span>汉堡</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FFF000">&#xe61b;</i>
                    <span>炸鸡</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #87CEEB">&#xe615;</i>
                    <span>烧腊</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #F4A460">&#xe62f;</i>
                    <span>火锅</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FF3030">&#xe76c;</i>
                    <span>准时</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #CAE1FF">&#xe73d;</i>
                    <span>地方</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FFFF00">&#xe75e;</i>
                    <span>东南</span>
                </li>
                <li class="item">
                    <i class="icon iconfont" style="color: #FA8072">&#xe760;</i>
                    <span>卤味</span></li>
            </ul>
        </mt-swipe-item>
      </mt-swipe>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.swipper {
    position: absolute;
    top: 125px;
    background-color: #fff;
    width: 100%;
    /* height: 100px; */
}
.mint-swipe {
    width: 100%;
    height: 150px;
    color: #504a4a;
    font-size: 30px;
    text-align: center;
    /* margin-bottom: 20px; */
}
.mint-swipe-item {
    width: 100%;
    height: 150px;
    line-height: 100px;
}
.items {
    margin-top: -20px;
    margin-left: -10px;
}
.item {
    list-style-type: none;
    float: left;
    margin-right: 40px;
    margin-bottom: -35px;
    height: 90px;
}
.item .iconfont {
    font-size: 24px;
}
.item span {
    font-size: 12px;
    margin-top: -80px;
    margin-left: -10px;
    position: absolute;
}
</style>
