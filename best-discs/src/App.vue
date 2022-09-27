<template>
  <div id="app">
         <HeaderContent/>
         <MainContent />
  </div>
</template>

<script>
import HeaderContent from './components/HeaderContent.vue';
import MainContent from './components/MainContent.vue';



export default {
  name: 'App',
  components: {
    HeaderContent,
    MainContent
}}
</script>

<style lang="scss">
  body{
    height: 100vh;
    display: flex;
    flex-direction: column;
  }
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
