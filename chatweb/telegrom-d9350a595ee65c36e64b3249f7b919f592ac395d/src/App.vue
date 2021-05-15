<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      todos: null,
    };
  },

};
</script>


<style>
html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
