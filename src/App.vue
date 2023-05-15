<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: 'App',
  mounted() {
    this.fetch();
  },
  methods: {
    async fetch() {
      const data = await axios.get('http://103.57.221.139/api/test')
      alert(data.data);
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
