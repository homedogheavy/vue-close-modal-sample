<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <CloseModal />
  </div>
</template>

<script>
import CloseModal from './components/CloseModal.vue'

export default {
  name: 'app',
  components: {
    CloseModal
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
