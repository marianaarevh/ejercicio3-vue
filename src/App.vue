<template>
  <ContadorSimple/>
</template>

<script>
import ContadorSimple from './components/ContadorSimple.vue'


export default {
  name: 'App',
  components: {
    ContadorSimple
  }
}
</script>

<style>
*{
  background-color: rgb(240, 240, 240);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
}
</style>
