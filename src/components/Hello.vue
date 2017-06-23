<template lang="pug">
  div
    h1 Hello, I am ViPro.
    article
      p This is my first github.io page.
      p Say 'Hello World!'
    div.pages
      mu-raised-button(@click="open(githubUrl)")
        img.github(:src="githubImg")
        | &nbsp;GitHub
      mu-raised-button(@click="open(codepenUrl)")
        img.codepen(:src="codepenImg")
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      codepenUrl: 'https://codepen.io/VdustR',
      codepenImg: require('@/assets/img/codepen.svg'),
      githubUrl: 'https://github.com/VdustR',
      githubImg: require('@/assets/img/github.svg')
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
.pages img
  height: 1em

.github
  filter: invert(100%)
</style>
