<template lang="pug">
  .home
    jumbotron(:content="content")
    slider
    //- img(alt="Vue logo" src="../assets/logo.png")
    //- hello-world(msg="Welcome to Your Vue.js App")
    section.section
      h2.title Yellow Leaf Hammocks
      p.lead Be Cool. Yellow Leaf Hammocks tells users about its product by describing how the hammocks empower artisan weavers and their families. The company breaks down different pieces of the story into sections that combine words and easily digestible graphics, painting a picture instead of big chunks of text. They're clear about why they're different: "Not a Charity," the page reads. And then: "This is the basis for a brighter future, built on a hand up, not a handout."
      p Yellow Leaf Hammocks tells users about its product by describing how the hammocks empower artisan weavers and their families. The company breaks down different pieces of the story into sections that combine words and easily digestible graphics, painting a picture instead of big chunks of text. They're clear about why they're different: "Not a Charity," the page reads. And then: "This is the basis for a brighter future, built on a hand up, not a handout."
</template>

<script>
import Jumbotron from '@/components/Jumbotron'
import Slider from '@/components/Slider'
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'home',
  components: {
    Slider,
    // HelloWorld,
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
