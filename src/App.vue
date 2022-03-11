<template>
  <div id="app">
    <SpotifyHeader />
  </div>
</template>

<script>
import SpotifyHeader from './components/SpotifyHeader.vue'

export default {
  name: 'App',
  components: {
    SpotifyHeader
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
