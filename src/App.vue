<template>
  <div id="app">
    <div @click="darkmode()">
      <h1 style="font-size: 300px; text-align: center; cursor: pointer;">
        YES
      </h1>
    </div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
  },
  data() {
    return {
      dark_mode: false,
    };
  },
  methods: {
    darkmode() {
      self.dark_mode = !self.dark_mode;
      self.dark_mode
        ? (document.body.className = "dark_mode")
        : (document.body.className = document.body.className.replace(
            "dark_mode",
            ""
          ));
    },
  },
};
</script>

<style>
.dark_mode {
  color: white;
  background-color: black;
}

#app {
  text-align: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
