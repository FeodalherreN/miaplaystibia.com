<template>
 <div id="app">
  <div class="text-center pt-5">
    <h1 class="h1 text-white display-1">Join the fun!</h1>
  </div>

  <TwitchPlayer />
 </div>
</template>

<script>
import TwitchPlayer from './components/TwitchPlayer.vue';

export default {
  name: 'App',
  components: {
    TwitchPlayer
  }
}
</script>

<style>
#app {
  height: 100%;
  width:100%;
  font-family: 'Roboto', sans-serif;
  background-color: #e6bcc6;
}

.h1 {
  font-weight: 800;
}
</style>
