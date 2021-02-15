<template>
  <div id="app">
    <user/>
    
  </div>
</template>

<script>
import userProfile from "./components/userProfile"

export default {
  name: 'App',
  components:{
    user:userProfile
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
