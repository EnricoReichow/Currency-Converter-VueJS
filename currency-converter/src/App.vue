<template>
  <div id="app">
    <h1 class="introMessage">Currency Converter</h1>
    <Converter currency-a="USD" currency-b="BRL" />
  </div>
</template>

<script>
import Converter from "./components/Converter.vue"

export default {
  name: 'App',
  components: {
    Converter
  }
}
</script>

<style>
body {
  background-color: linear-gradient(89.7deg, rgb(0, 32, 95) 2.8%, rgb(132, 53, 142) 97.8%);
  ;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  display: flex;
  justify-content: center;
  align-items: center;
}

.introMessage{
  padding-top: 20%;
  color: rgb(255, 255, 255);
}
</style>
