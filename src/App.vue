<template>
  <div id="app">
    <Navbar/>
    <router-view/>
  </div>
</template>
<script>

import Navbar from './components/Navbar.vue'
export default {
  components: {
    Navbar
  },
  created () {
    this.$store.dispatch('fetchCart')
    this.$store.dispatch('isLoggedIn')
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
  margin-bottom: 5%;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

.swal-wide{
    width:500px !important;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
