<template>
  <div class="top_nav">
      <div class="logo">LOGO</div>
      <ul class="menu">
        <li>菜单1</li>
        <li>菜单2</li>
      </ul>
    </div>
</template>
<style lang="scss" scoped>
 .top_nav{
   width:100%;
   height:100px;
   display:flex;
   justify-content: space-between;
   padding: 0 50px;
   box-sizing: border-box;
   align-items: center;
   background: pink;
   .menu{
     display: flex;
     justify-content: flex-start;
     align-items: center;
     li{
       margin-left: 50px;
     }
   }
 } 
</style>