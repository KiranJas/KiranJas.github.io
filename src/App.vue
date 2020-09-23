<template>
  <div id="app">
    <Header/>
    <Subheader/>
    <router-view/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Subheader from "./components/Subheader";

export default {
  name: "app",
  components: {
    Header,
    Subheader
  }
}
</script>


<style>
/* @import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,500;1,500&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500&family=Roboto:wght@400;500&display=swap');

#app {
  font-family: 'Roboto', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
