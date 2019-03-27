<template>
  <div id="app">
    <Phone/>
  </div>
</template>

<script>
import Phone from './components/Phone.vue'

export default {
  name: 'app',
  components: {
    Phone
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* margin-top: 60px; */
}
</style>
