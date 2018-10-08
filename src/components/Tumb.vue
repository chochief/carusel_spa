<template lang="pug">
  a.tumb(
    :href="href"
    target="_blank"
    :style="style"
  )
</template>

<script>
export default {
  props: ['href', 'src'],
  // data () {
  //   return {

  //   }
  // },
  computed: {
    style () {
      return {
        backgroundImage: `url(${this.src})`
      }
    }
  }
}
</script>

<style lang="scss">
.tumb {
  display: block;
  min-height: 200px;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  border-radius: 4px;
}
</style>
