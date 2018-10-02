<template lang="pug">
  .wrap(id="app")
    sticky-header
    .content
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
  overflow-y: scroll;
}

.wrap {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.content {
  flex: 1 0 auto;
  overflow: hidden;
  margin: 80px 0;
  padding: 30px;
  // min-height: 2000px;
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
</style>
