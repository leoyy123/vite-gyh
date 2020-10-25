<template>
  <div>
    <Topnav></Topnav>
    <div class="content">
      <aside v-if="asideVisible">
        <h2>组件列表</h2>
        <ol>
          <li>
            <router-link to="/doc/switch">Switch 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/button">Button 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/dialog">Dialog 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/tabs">Tabs 组件</router-link>
          </li>
        </ol>
      </aside>
      <main>主内容</main>
    </div>
  </div>
</template>
<script lang="ts">
import Topnav from '../components/Topnav.vue';
import {inject,Ref} from 'vue';
export default {
  components:{
    Topnav
  },
  setup(){
    const asideVisible =  inject<Ref<boolean>>('asideVisible');
    console.log('asidVI',asideVisible);
    return {asideVisible}
  }
}
</script>
<style lang="scss" scoped>
  aside{
    line-height: 50px;
    background: lightblue;
    width: 160px;
    text-align: left;
    padding-left: 20px;
  }
  @media (max-width:500px){
    aside{
    position: fixed;
    top: 0;
    left: 0;
    padding-top: 120px;


    }
  }
</style>