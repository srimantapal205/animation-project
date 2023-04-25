<template>
  <button type="button" @click="flag = !flag">Animation Text</button>
  <img alt="Vue logo" src="./assets/logo.png">
  <transition name="fade" mode="out-in">
    
    <HelloWorld v-if="flag" key="main"/>
    <about v-else key="secondary"/>
  </transition>
  
</template>

<script>
import about from './components/about.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    about
  },
  data() {
    return {
      flag: false
    }
  },

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
.fade-enter-from{
  opacity: 0;
}
.fade-enter-active{
  transition:  all 3s linear;
}
.fade-leave-to{
  transition:  all 3s linear;
  opacity: 0;
}
</style>
