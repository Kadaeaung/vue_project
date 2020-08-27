<template>
  <div id="app">
     <!-- <img alt="Vue logo" src="./assets/logo.png"> --> 
<!--     <HelloWorld msg="Welcome to Your Vue.js App"/> -->
<div>
  <b-tabs content-class="mt-3">
    <b-tab title="Testing" active>  <Testing></Testing></b-tab>
    <b-tab title="HomeWorks">  <HomeWork></HomeWork></b-tab>

  </b-tabs>
</div>


  </div>

</template>

<script>
 import Testing from './components/Testing.vue'
 import HomeWork from './components/HomeWork.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Testing,
    HomeWork


  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
