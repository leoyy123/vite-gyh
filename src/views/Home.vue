<template>
  <div class="home">
    <Topnav></Topnav>
    <div class="banner">
      <h1>小郭ui</h1>
      <h2>一个蛇皮的ui框架</h2>
      <p class="actions">
        <a href="https://github.com/leoyy123/vite-gyh">GitHub</a>
        <router-link to="/doc">开始</router-link>
      </p>
    </div>
  </div>
</template>
<script lang="ts">
import Topnav from '../components/Topnav.vue';
export default {
  components:{
    Topnav
  }
}
</script>
<style lang="scss" scoped>
  .banner{
    width: 100%;
    padding: 50px 0;
    background: lightgreen;
    height: 100%;
    .actions{
      margin-top: 20px;
      a{
      padding: 5px;
      border-radius: 20px;
      background: #fff;
      margin-right: 20px;
    }
    }
    
  }
  .home{
    height: 100%;
  }
</style>