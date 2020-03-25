<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{ tag }}</h1>
    <HelloWorld msg="Welcome to Your Vue.js App" something="Hai"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import {
  AZURE_TOKEN,
} from './constants'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  computed: {
    tag (){
      // return process.env.NODE_ENV;
      // return process.env.VUE_APP_SECRET_CODE;
      // return process.env.VUE_APP_SOMETHING;
      console.log(AZURE_TOKEN);
      return AZURE_TOKEN;
    }
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
