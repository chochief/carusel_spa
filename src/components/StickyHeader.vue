<template lang="pug">
  header.header(id="header")
    .container
      .logo(id="logo") Carusel SPA
      nav.navbar
        router-link.nav__item(to="/") Home
        router-link.nav__item(to="/about") About US
        router-link.nav__item(to="/contact") Contact Us
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
.header {
  width: 100%;
  height: 80px;
  background-color: #446cb3;
  color: #ffffff;
  line-height: 80px;
  position: fixed;
  z-index: 100;
  top: 0;
  transition: all 0.5s ease;
  &.sticky {
    background-color: rgba(211,84,0,.9);
    height: 50px;
    line-height: 50px;
    & .logo {
      font-size: 25px;
    }
    & .nav__item {
      font-size: 15px;
    }
  }
}

.container {
  width: 100%;
  max-width: 1024px;
  margin: 0 auto;
}

.logo {
  font-family: 'Oswald', sans-serif;
  font-size: 40px;
  float: left;
  margin: 0 10px;
}

.navbar {
  float: right;
}

.nav__item {
  font-size: 22px;
  color: #ffffff;
  text-decoration: none;
  margin: 0 15px;
  &:hover {
    color: #fbce2a;
  }
  &.router-link-exact-active {
    color: #fbce2a;
  }
}
</style>
