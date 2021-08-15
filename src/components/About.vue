<template>
  <section class="about-us" id="about">
    <div class="description">
      <div>
        <span class="line" />
        <h2>About Us</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat.
        </p>
      </div>
      <div class="description--image">
        <img src="@/assets/images/about-us.png" alt="about us" />
        <span class="side-decoration" />
      </div>
    </div>
    <Items />
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Items from './Items.vue'

export default defineComponent({
  name: 'About',
  components: { Items },
})
</script>

<style lang="stylus" scoped>
h2
  font-size 3.6rem

  @media (min-width: 1024px)
    font-size 4.4rem

p
  font-size 1.3rem
  line-height 2
  margin 1.6rem 0

  @media (min-width: 768px)
    width 92%

  @media (min-width: 1024px)
    font-size 1.4rem
    line-height 1.75
    max-width 500px

.about-us
  @media (max-width: 767px)
    padding 2.4rem 0

.description
  @media (min-width: 768px)
    align-items center
    display grid
    grid-template-columns 1fr 1fr

  @media (max-width: 767px)
    text-align center

.line
  @media (max-width: 767px)
    margin 0 auto

.description--image
  position relative

.side-decoration
  top 28%
  right -42px

  @media (max-width: 767px)
    display none
</style>
