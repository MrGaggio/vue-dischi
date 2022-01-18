<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header />
    <Main />
    <Search />
    
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Search from './components/Search.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header,
    Main,
    Search
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
