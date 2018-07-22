<template>
  <div id="app">
    <Clock />
  </div>
</template>

<script>
import Clock from './components/Clock'

export default {
  name: 'App',
  components: {
    Clock
  },
  created () {
    
  },

  mounted () {
    console.log('compontent mounted');
  }
}
</script>

<style>
body, html {
  width: 100%;
  height: 100%;
}

body {
  background: -webkit-linear-gradient( LightSteelBlue, LightSalmon);
  background: -o-linear-gradient( LightSteelBlue, LightSalmon);
  background: -moz-linear-gradient( LightSteelBlue, LightSalmon);
  background: linear-gradient( LightSteelBlue, LightSalmon);
}



</style>
