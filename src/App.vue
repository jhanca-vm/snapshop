<template>
  <Header />
  <main>
    <Hero />
    <div class="x-o" />
    <About />
    <HowItWorks />
  </main>
  <Footer />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import HowItWorks from './components/HowItWorks.vue'
import Footer from './components/Footer.vue'

export default defineComponent({
  name: 'App',
  components: { Header, Hero, About, HowItWorks, Footer },
})
</script>

<style lang="stylus">
font(name)
  font-display swap
  font-family 'Poppins'
  src url('./assets/fonts/' + name + '.ttf') format('truetype')

decoration(image, size, position)
  background url('./assets/images/' + image + '.svg') no-repeat
  background-size contain
  height size
  position position

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
  scroll-behavior smooth

body
  font-size 1.6rem

main
  padding 0 32px

  @media (min-width: 540px)
    padding 0 60px

  @media (min-width: 1024px)
    padding 0 80px

h1, h2, h3
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

.line
  background-color #fbbb21
  display block
  height 0.3rem
  width 2.4rem

.x
  decoration('x', 44px, absolute)
  width 44px

.x-o
  decoration('x-o', 60px, relative)
  left -40px
  top -20px

  @media (max-width: 767px)
    display none

.side-decoration, .side-patron
  display block

.side-decoration
  decoration('side-decoration', 150px, absolute)
  width 15px

.side-patron
  decoration('side-patron', 160px, absolute)
  width 46px
</style>
