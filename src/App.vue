<template>
  <router-view></router-view>
</template>

<script lang="ts">
import {ref,provide}  from 'vue';
import {router} from './router';
export default {
  name: 'App',
  setup(){
    const width = document.documentElement.clientWidth
    const asideVisible = ref(width>500?true:false);
    provide('asideVisible',asideVisible);
    router.afterEach(()=>{
      console.log(width)
      if(width>500){
        return;
      }
      asideVisible.value = false;
    })
  }
 
}
</script>
