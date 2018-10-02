<template  lang="pug">
  .wrap(id="app")
    .content
      sticky-header
      div(id="nav")
        router-link(to="/") Home
        router-link(to="/about") About
      router-view
    footer.footer Hi! It's the Carusel SPA
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
* {
  margin: 0;
}

html, body {
  height: 100%;
}

body {
  // font-family: 'Oswald', sans-serif;
  font-family: 'Roboto Condensed', sans-serif;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  color: #2c3e50;
}

.wrap {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.content {
  flex: 1 0 auto;
  min-height: 2000px;
  overflow: hidden;
}

.footer {
  flex: 0 0 auto;
  width: 100%;
  height: 40px;
  background-color: #2c3e50;
  text-align: center;
  color: white;
  line-height: 40px;
}

#nav {
  margin: 80px 0;
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
