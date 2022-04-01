<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import axios from "axios";

export default {
  name: "Home",
  data() {
    return {};
  },
  mounted() {
    this.getTasks();
  },
  methods: {
    getTasks() {
      axios({
        method: "get",
        url: "http://127.0.0.1:8000/tasks/",
        auth: {
          username: "tao",
          password: "taotaotao",
        },
      }).then((response) => (this.tasks = response.data));
    },
  },
  components: {
    HelloWorld,
  },
};
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
