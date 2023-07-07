<template>
 <div id="app" :class="{ 'dark-mode': darkMode }">
    <MainContent />
  </div>
  <!-- <MainContent/> -->
</template>

<script>
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    MainContent,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  /* font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif; */
  /* -webkit-font-smoothing: antialiased; */
  /* -moz-osx-font-smoothing: grayscale; */
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
}

html {
  scroll-behavior: smooth;
}

body {
  background-color: #080808;
  background-color: #F6F4F1;
  /* background-color: rgb(0, 0, 0); */
}

</style>
