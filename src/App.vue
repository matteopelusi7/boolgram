<template>
  <div id="app">
    <NavBar />

    <MainContent />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    MainContent
  }
}
</script>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: -8px;
  padding: 0;
  box-sizing: border-box;
}

</style>
