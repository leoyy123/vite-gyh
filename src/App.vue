<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" /> -->
  <div>导航栏| <router-link to="/">Frank</router-link><router-link to="/frank2">Frank2</router-link></div>
  <hr/>
  <!-- <Frank></Frank> -->
  <router-view></router-view>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import Frank from './components/Frank.vue'

export default {
  name: 'App',
 
}
</script>
