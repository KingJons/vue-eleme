<template>
  <div class="page-tabber">
      <div class="page-wrap">
            
      
          <mt-tab-container class="page-tabber_container" v-model="selected">
            <mt-tab-container-item id="外卖">
                <el-home></el-home>
            </mt-tab-container-item>
            <mt-tab-container-item id="发现">
                <el-found></el-found>
            </mt-tab-container-item>
            <mt-tab-container-item id="订单">
                <el-order></el-order>
            </mt-tab-container-item>
            <mt-tab-container-item id="我的">
                <el-mine></el-mine>
            </mt-tab-container-item>
          </mt-tab-container>
      </div>
      <mt-tabbar v-model="selected" fixed class="tabbar">
        <mt-tab-item id="外卖">
            <i class="icon iconfont">&#xe722;</i><br>
            <span>外卖</span>
        </mt-tab-item>
        <mt-tab-item id="发现">
            <i class="icon iconfont">&#xe69d;</i><br>发现
        </mt-tab-item>
        <mt-tab-item id="订单">
            <i class="icon iconfont">&#xe612;</i><br>订单
        </mt-tab-item>
        <mt-tab-item id="我的">
            <i class="icon iconfont">&#xe63f;</i><br>我的
        </mt-tab-item>
      </mt-tabbar>
  </div>
</template>

<script>
import Home from '@/components/pages/home'
import Found from '@/components/pages/found'
import Mine from '@/components/pages/mine'
import Order from '@/components/pages/order'
export default {
    name: 'page-tabbar',
    data() {
        return {
            selected: '外卖'
        };
    },
    components: {
        'el-home': Home,
        'el-found': Found,
        'el-mine': Mine,
        'el-order': Order
    }
}
</script>

<style scoped>
.page-tabbar {
    overflow: hidden;
    height: 100vh;
}
.page-wrap {
    overflow: auto;
    height: 100%;
    padding-bottom: 100px;
    
}
/* .page-tabber_container {
    position: absolute;
    width: 300px;
    top: 60px;
    left: 20px;   
} */


.tabbar {
    height: 50px;
}
.iconfont {
    font-size: 20px;
}
</style>
