<template>
    
  <div class="home">
    <div class="location">
        <i class="icon iconfont">&#xe611;</i> 
        <span>江西财经大学</span>   
    </div>
    <mt-search class="search" cancel-text="取消" placeholder="免费领取你的专属红包" v-model="value" :result="filterResult"></mt-search>
    <div class="text">
      <span>鸡排</span>
      <span>烤鸡</span>
      <span>鸡腿</span>
      <span>烧烤</span>
      <span>会员领红包</span>
      <span>兰州拉面</span>
    </div>
    <el-swipper></el-swipper>
    <el-swipper-auto></el-swipper-auto>
    <div class="activity">
      <div class="left">
        <h3>限时抢购</h3>
        <p class="text2">超值美味 9.9元起</p>
        <div class="number">
          <span>4455人</span>正在抢>
        </div>
        <img src="http://fuss10.elemecdn.com/b/e1/0fa0ed514c093a7138b0b9a50d61fpng.png" alt="">
      </div>
      <div class="right">
        <h3>品质套餐</h3>
        <p class="text2">搭配齐全吃得好</p>
        <div class="number">
          <span>立即抢购></span>
        </div>
        <img src="http://fuss10.elemecdn.com/d/d4/16ff085900d62b8d60fa7e9c6b65dpng.png" alt="">
      </div>
    </div>
    <el-scroll></el-scroll>
  </div>
  
</template>

<script>
import Swipper from '@/components/common/swipper'
import SwipperAuto from '@/components/common/swipper-auto'
import Scroll from '@/components/common/scroll'
export default {
  name: 'home',
  data() {
    return {
      value: '',
      defaultResult: [
        'Apple',  
        'Banana',  
        'Orange',  
        'Durian',  
        'Lemon',  
        'Peach',  
        'Cherry',  
        'Berry',  
        'Core',  
        'Fig',  
        'Haw',  
        'Melon',  
        'Plum',  
        'Pear',  
        'Peanut',  
        'Other'  
      ]
    }
    
  },
  components: {
      'el-swipper': Swipper,
      'el-swipper-auto': SwipperAuto,
      'el-scroll': Scroll
  },
  computed: {
    filterResult() {
      return this.defaultResult.filter(value => new RegExp(this.value, 'i').test(value));
    }
  }
}
</script>

<style scoped>
.text {
  position: absolute;
  top:105px;
  left: 20px;
  font-size: 12px;
  float: left;
  color: #f9f9f9;
}
.text span {
  margin-right: 16px;
}
.location {
    padding-left: 10px;
    padding-top: 20px;
}
.activity {
  width: 100%;
  height: 130px;
  background-color: #ffffff;
  position: absolute;
  top: 365px;
}
.activity .left {
  width: 45%;
  padding-left: 10px;
  height: 120px;
  background-color: #f4f4f4;
  margin-top: -13px;
  margin-left: 5px;
}
.activity .left h3{
  color: #e81919;
  padding-top: 10px;
  font-size: 18px;
}
.activity .left .text2 {
  font-size: 13px;
  margin-top: -15px;
  color: #777777;
}
.activity .left .number {
  margin-top: -8px;
  font-size: 12px;
}
.activity .left .number span {
  color:#e81919;
  font-weight: 600;
}
.activity .left img {
  width: 85px;
  height: 55px;
  margin-left: 70px;
  margin-top: -10px;
}
.activity .right {
  width: 45%;
  padding-left: 10px;
  height: 120px;
  background-color: #f4f4f4;
  margin-top: -139px;
  margin-left: 180px;
}
.activity .right h3{
  color: #333333;
  padding-top: 10px;
  font-size: 18px;
}
.activity .right .text2 {
  font-size: 13px;
  margin-top: -15px;
  color: #777777;
}
.activity .right .number {
  margin-top: -8px;
  font-size: 12px;
}
.activity .right .number span {
  color:#af8260;
  font-weight: 600;
}
.activity .right img {
  width: 85px;
  height: 55px;
  margin-left: 70px;
  margin-top: -10px;
}
</style>
