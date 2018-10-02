<template lang="pug">
  .wrapper(id="wrapper")
    header.header(id="header")
      .container
        .logo(id="logo") Carusel SPA
        nav.navbar
          a(href="#").nav__item Home
          a(href="#").nav__item About US
          a(href="#").nav__item Contact Us
</template>

<script>
export default {
  methods: {
    handleScroll () {
      let header = document.getElementById('header')
      if (window.scrollY > 1) {
        header.classList.add('sticky')
      } else {
        header.classList.remove('sticky')
      }
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll)
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="scss" scoped>
.wrapper {
    width: 100%;
    height: auto;
    padding: 0;
    margin: 0;
    overflow: hidden;
    min-height: 2000px;
  }

.header {
  width: 100%;
  height: 80px;
  background-color: #446cb3;
  color: #ffffff;
  line-height: 80px;
  position: fixed;
  top: 0;
  transition: all 0.5s ease;
  &.sticky {
    background-color: rgba(211,84,0,.9);
    height: 50px;
    line-height: 50px;
    & .logo {
      font-size: 22px;
    }
    & .nav__item {
      font-size: 14px;
    }
  }
}

.container {
  width: 100%;
  max-width: 1024px;
  margin: 0 auto;
}

.logo {
  font-family: oswald;
  font-size: 40px;
  float: left;
}

.navbar {
  float: right;
  font-family: Helvetica;
}

.nav__item {
  color: #ffffff;
  text-decoration: none;
  margin: 0 15px;
  &:hover {
    color: #fbce2a;
  }
}
</style>
