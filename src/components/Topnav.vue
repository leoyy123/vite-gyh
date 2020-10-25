<template>
  <div class="top_nav">
      <div class="logo" >LOGO</div>
      <ul class="menu">
        <li>菜单1</li>
        <li>菜单2</li>
      </ul>
      <div class="toggle_aside" @click="toggleAside"></div>
    </div>
</template>
<script lang="ts">
import {inject,Ref} from 'vue'
export default {
  name:'topnav',
  setup(){
    const asideVisible =  inject<Ref<boolean>>('asideVisible');
    console.log('asidVI',asideVisible);
   const toggleAside=()=>{
     asideVisible.value = !asideVisible.value;
   }
   return {toggleAside}
  }
}
</script>
<style lang="scss" scoped>
 .top_nav{
   width:100%;
   height:100px;
   display:flex;
   justify-content: center;
   padding: 0 50px;
   box-sizing: border-box;
   align-items: center;
   background: pink;
   position: relative;
   z-index: 10;
    .logo{
      max-width: 6rem;
      margin-right: auto;
    }
   .menu{
     display: flex;
     justify-content: flex-start;
     align-items: center;
     li{
       margin-left: 50px;
     }
   }
 } 

 .toggle_aside{
   width: 24px;
   height: 24px;
   background: red;
   position: absolute;
   left: 20px;
   top: 50px;
   transform: translateY(-50%);
   display: none;
 }
 @media (max-width:500px){
   .top_nav .menu{
     display: none;
   }
   .logo{
     margin: 0 auto ;
   }
   .toggle_aside{
     display: block;
   }
 }
</style>