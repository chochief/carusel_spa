<template lang="pug">
  .jumbotron
    h1.title {{ content.title }}
    p.lead {{ content.lead }}
    hr.hr
    p.text {{ content.text }}
    router-link(:to="content.url")
      button.btn {{ content.btn }}
</template>

<script>
export default {
  props: ['content']
}
</script>

<style lang="scss" scoped>
.jumbotron {
  position: relative;
  margin: 24px 10px;
  padding: 64px 32px;
  border-radius: 4px;
  background-color: #e9ecef;
  & .title {
    font-family: 'Oswald', sans-serif;
    font-size: 56px;
    line-height: 1.2;
  }
  & .lead {
    font-size: 24px;
    margin-bottom: 16px;
  }
  & .hr {
    border: 0;
    border-top: 1px solid rgba(0,0,0,.1);
    margin: 20px 0;
  }
  & .text {
    margin-bottom: 16px;
  }
  & .btn {
    position: relative;
    z-index: 1;
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
}
</style>
