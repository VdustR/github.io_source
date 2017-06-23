<template lang="pug">
  div
    h1 Hello, I am ViPro.
    article
      p This is my first github.io page.
      p Say 'Hello World!'
    div
      mu-raised-button(@click="open(codepenUrl)")
        img.codepen(:src="codepenImg")
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      codepenUrl: 'https://codepen.io/VdustR',
      codepenImg: require('@/assets/img/codepen.svg')
    }
  },

  methods: {
    open (url) {
      open(url, '_blank')
    }
  }
}
</script>

<style lang="sass" scoped>
.codepen
  height: 1em
</style>
