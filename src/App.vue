<template>
  <div id="app">
    <sticky-header />
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
import StickyHeader from './components/StickyHeader'
export default {
  components: {
    StickyHeader
  }
}
</script>

<style lang="scss">
body {
  // font-family: 'Oswald', sans-serif;
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 16px;
}

#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
