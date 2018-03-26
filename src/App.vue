<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  background-color: #029ffe;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 130px;
}
</style>
