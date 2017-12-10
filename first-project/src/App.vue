<template>
  <div id="app">
    <firstcomponent />
    <router-view/>
    <parent />
    <one />
    <two />
  </div>
</template>

<script>
import parent from './components/parent'
import firstcomponent from './components/firstcomponent'
import one from './components/one'
import two from "./components/two"
import bus from './components/bus'
export default {
  name: 'app',
  components: { 
    parent,
    firstcomponent,
    one,
    two,
    bus
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
