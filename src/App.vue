<template>
  <ContadorSimple/>
  <ToDo/>
</template>

<script>
import ContadorSimple from './components/ContadorSimple.vue'
import ToDo from './components/ToDo.vue'


export default {
  name: 'App',
  components: {
    ContadorSimple,
    ToDo
  }
}
</script>

<style>
*{
  background-color: white;
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
