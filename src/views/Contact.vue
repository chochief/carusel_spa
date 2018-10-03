<template lang="pug">
  form.form
    h1.title Contact Us
    p.lead Write to us about your opinion. This is a simple hero unit, a simple jumbotron-style component for calling extra attention to featured content or information.
    hr.hr
    input(type="text" v-model="name")
    p.label {{ nameLabel }}
    input(type="text" v-model="phone")
    p.label {{ phoneLabel }}
    textarea(v-model="message" rows="7")
    p.label {{ messageLabel }}
    button.btn Send
    button.btn Clear
</template>

<script>
export default {
  data () {
    return {
      name: 'Bruce',
      nameLabel: 'Write your name',
      phone: '+7 555 55 55',
      phoneLabel: 'Enter your phone number',
      message: 'Yellow Leaf Hammocks tells users about its product by describing how the hammocks empower artisan weavers and their families. The company breaks down different pieces of the story into sections that combine words and easily digestible graphics, painting a picture instead of big chunks of text. They\'re clear about why they\'re different: "Not a Charity," the page reads. And then: "This is the basis for a brighter future, built on a hand up, not a handout."',
      messageLabel: 'Write your message'
    }
  }
}
</script>

<style lang="scss" scoped>
.form {
  position: relative;
  z-index: 1;
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
}

input, textarea {
  display: block;
  width: 100%;
  outline: none;
  border: 1px solid #e9ecef;
  border-radius: 4px;
  font-size: 24px;
  padding: 12px 21px;
  box-sizing: border-box;
}

textarea {
  resize: none;
  font-size: 21px;
}

.label {
  margin-bottom: 16px;
  padding: 6px 21px 0;
  text-align: center;
}
</style>
