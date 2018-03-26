<template>
  <div class="scroll">
      <div class="title">
          <p>—— 推荐商家 ——</p>
      </div>
      <ul v-infinite-scroll="loadMore"  infinite-scroll-distance="20" infinite-scroll-disabled="loading">
        <li v-for="(item,index) in list" :key="index">
            <div class="left"><img :src="item.img" alt=""></div>
            <div class="right">
                <p class="stitle">{{item.name}}({{item.adress}})</p>
                <el-rate></el-rate>
                <p class="star">
                    {{item.star}}
                    月售{{item.sales}}份
                </p>
                <p class="send">
                    ￥{{item.send}}起送 | 配送费{{item.fee}}元
                </p>
                <p class="distance">
                    {{item.distance}} | {{item.time}}分钟
                </p>
            </div>
            <p class="activity1">
                {{item.activity1}}  
            </p>   
            <p class="activity2">
                {{item.activity2}}  
            </p>          
        </li>
      </ul>
  </div>
</template>

<script>
import axios from 'axios'
import ElRate from './ElRate'
export default {
    data() {
        return {
            list: [],
            loading: false

        }
    },
    mounted: function() {
        axios.get('https://www.easy-mock.com/mock/5ab5fae51a094046dab2cbf2/businessInfo/businessInfos')
        .then(response => this.list = response.data.data.list)
        .catch(error => console.log(error))
    },
    computed: {
        loadMore() {
            this.loading = true;
            setTimeout(() => {
                let last = this.list[this.list.length - 1];
                // console.log(last);
                for(let i = 1; i <= 10; i++) {
                    this.list.push(last);
                }
                this.loading = false;
            },2500);
        }
    },
    components: {
        'el-rate': ElRate
    }
}
</script>

<style>
.scroll {
    /* position: absolute;  */
    margin-top: -180px;  
    height: 100%;
    width: 100%;
    overflow-y:scroll;
}
.scroll .title {
    margin-left: 120px;
    font-size: 14px;
    color: #383131;
    width: 100%;
    font-weight:550;
}
.scroll ul {
    margin-top: 20px;
    padding: 0;
}
.scroll ul li{
    list-style-type: none;
    width: 100%;
    height: 120px;
    border-bottom: 1px solid #ccc;
}
.scroll ul li .left {
    width: 20%;
}
.scroll ul li img {
    width: 60px;
    height: 50px;
    padding-top: 10px;
    padding-left: 10px;
}
.scroll ul li .right {
    border-bottom: 1px solid #383131;
    width: 80%;
    margin-left: 80px;
}
.scroll ul li .stitle {
    margin-top: -56px;
    /* margin-left: 80px; */
    font-size: 15px;
    font-weight: 550;
}
.scroll ul li .star {
    margin-top: -16px;
    font-size: 10px;
    margin-left: 55px;
    color: #383131;
}
.scroll ul li .send {
    margin-top: -5px;
    font-size: 10px;
    /* margin-left: 10px; */
    color: #383131;
}
.scroll ul li .distance {
    margin-top: -23px;
    margin-left: 200px;
    font-size: 10px;
    color: #383131;
}
.scroll ul li .activity1 {
    margin-left: 80px;
    font-size: 10px;
    margin-top: 5px;
}
.scroll ul li .activity2 {
    margin-left: 80px;
    font-size: 10px;
    margin-top: -5px;
}
</style>
