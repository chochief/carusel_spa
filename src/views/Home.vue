<template lang="pug">
  .home
    jumbotron(:content="content")
    img(alt="Vue logo" src="../assets/logo.png")
    hello-world(msg="Welcome to Your Vue.js App")
</template>

<script>
import Jumbotron from '@/components/Jumbotron'
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    Jumbotron
  },
  data () {
    return {
      content: {
        title: 'Welcome to Carusel SPA!',
        lead: 'This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.',
        text: 'It uses utility classes for typography and spacing to space content out within the larger container.',
        btn: 'Learn more',
        url: '/about'
      }
    }
  }
}
</script>
