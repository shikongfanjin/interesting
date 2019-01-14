<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app',
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

  html, body {
    margin: 0;
    width: 100%;
    height: 100%;
  }

  *, :after, :before {
    box-sizing: border-box;
  }
</style>
