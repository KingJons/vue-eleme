<template>
  <div class="swipper-auto">
    <mt-swipe :auto="4000">
        <mt-swipe-item>
            <img src="http://fuss10.elemecdn.com/0/e7/64044fb6df771e9cb42196ae3eeeejpeg.jpeg" alt="">
        </mt-swipe-item>
        <mt-swipe-item>
            <img src="http://fuss10.elemecdn.com/3/72/16598634401205f39786536114539jpeg.jpeg" alt="">
        </mt-swipe-item>
    </mt-swipe>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped> 
.swipper-auto {
    position: absolute;
    top: 270px;
    background-color: #fff;
    width: 100%;
}
.mint-swipe {
    width: 100%;
    height: 100px;
    color: #fff;
    font-size: 30px;
    text-align: center;
    /* margin-bottom: 20px; */
}
.mint-swipe-item {
    width: 100%;
    height: 100px;
    line-height: 100px;
}
.mint-swipe-item img{
    width: 340px;
    height: 90px;
    margin-top: 5px;
}
</style>
