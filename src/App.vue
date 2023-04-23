<template>
  <div id="app">
    <h1>Hello World</h1>
    <!-- <test msg="Adios"/> -->
    <user/>
  </div>
</template>

<script>

import test from "./components/test.vue";
import user from "./components/user.vue";

export default {

  name: 'App',
  components: {
    test,
    user
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
