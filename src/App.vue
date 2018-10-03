<template lang="pug">
  .wrap(id="app")
    sticky-header
    .content
      router-view
    footer.footer Hi! We present you the Carousel SPA
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
  box-sizing: border-box;
}

.wrap {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.content {
  flex: 1 0 auto;
  overflow: hidden;
  margin: 80px auto 50px;
  max-width: 1024px;
  padding: 30px;
  // min-height: 2000px;
}

.footer {
  flex: 0 0 auto;
  width: 100%;
  height: 60px;
  background-color: #2c3e50;
  text-align: center;
  color: white;
  line-height: 60px;
}

.section {
  position: relative;
  z-index: 1;
  margin: 24px 10px;
  padding: 64px 32px;
  border-radius: 4px;
  border: 1px dashed #e9ecef;
  // background-color: #e9ecef;
}

.title {
  font-family: 'Oswald', sans-serif;
  font-size: 56px;
  line-height: 1.2;
  margin: 22px 0
}

.lead {
  font-size: 24px;
  margin-bottom: 16px;
}

.hr {
  border: 0;
  border-top: 1px solid rgba(0,0,0,.1);
  margin: 20px 0;
}

.text {
  margin-bottom: 16px;
}

.btn {
  position: relative;
  z-index: 1;
  margin-right: 10px;
  padding: 12px 16px;
  border-radius: 4px;
  cursor: pointer;
  background-color: #335185;
  color: white;
  outline: none;
  border: 0;
  font-size: 22px;
  transition: all 0.5s ease;

  &:hover {
    color: #fbce2a;
  }

  &:focus {
    top: 2px;
  }
}
</style>
