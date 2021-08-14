<template>
  <Header />
  <main>
    <Hero />
    <div class="x-o" />
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'

export default defineComponent({
  name: 'App',
  components: { Header, Hero },
})
</script>

<style lang="stylus">
font(name)
  font-display swap
  font-family 'Poppins'
  src url('./assets/fonts/' + name + '.ttf') format('truetype')

decoration(image, size)
  background url('./assets/images/' + image + '.svg') no-repeat
  background-size contain
  height size

@font-face
  font('Poppins-Regular')

@font-face
  font('Poppins-Bold')
  font-weight bold

*
  box-sizing border-box
  font-family 'Poppins', sans-serif
  margin 0
  padding 0

html, body
  min-width 320px

html
  color #171717
  font-size 62.5%

body
  font-size 1.6rem

main
  padding 0 32px

  @media (min-width: 540px)
    padding 0 60px

  @media (min-width: 1024px)
    padding 0 80px

h1, h2
  color #0d72fa

img
  width 100%

input, button
  background none
  border none
  color inherit
  font-size inherit

input
  outline none

button
  cursor pointer

.x
  decoration('x', 44px)
  position absolute
  width 44px

.x-o
  decoration('x-o', 62px)
  left -40px
  position relative
  top -20px

  @media (max-width: 767px)
    display none
</style>
