<template>
  <section id="how-it-works">
    <span class="line" />
    <h2>How It Works</h2>
    <div>
      <article v-for="{ id, title, description, image } in data" :key="id">
        <b>{{ id }}</b>
        <span class="line" />
        <h3>{{ title }}</h3>
        <p>{{ description }}</p>
        <img :src="require(`@/assets/images/${image}`)" alt="" />
      </article>
    </div>
    <span class="side-decoration first" />
    <span class="side-patron" />
    <span class="side-decoration second" />
    <span class="side-decoration third" />
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import data from '@/data/how-it-itworks.json'

export default defineComponent({
  name: 'HowItWorks',
  setup() {
    return { data }
  },
})
</script>

<style lang="stylus" scoped>
section
  position relative
  padding 3.2rem 0 2rem
  text-align center

  @media (min-width: 768px)
    padding-top 5.2rem

h2
  font-size 3.6rem
  margin-bottom 3.2rem

  @media (min-width: 1024px)
    font-size 4.4rem
    margin-bottom 4.4rem

div
  display grid
  row-gap 4rem

  @media (min-width: 640px)
    column-gap 48px
    grid-template-columns 1fr 1fr
    row-gap 4.8rem

  @media (min-width: 1024px)
    grid-template-columns repeat(6, 1fr)

b
  align-items center
  background-color #0d72fa
  border-radius 50%
  color white
  display inline-flex
  font-size 2.6rem
  justify-content center
  height 4.8rem
  width 4.8rem

h3
  font-size 2rem

p
  font-size 1.3rem
  margin 1.2rem auto 2.4rem
  max-width 320px

  @media (min-width: 540px)
    font-size 1.4rem

img
  object-fit contain
  max-height 170px

article
  @media (min-width: 640px)
    &:last-of-type
      grid-column span 2

  @media (min-width: 1024px)
    grid-column span 2
    &:nth-of-type(4)
      grid-column 2 / span 2
    &:nth-of-type(5)
      grid-column 4 / span 2

.line
  margin 1rem auto 0.1rem

.side-decoration, .side-patron
  @media (max-width: 767px)
    display none

.side-decoration.first,
.side-decoration.third
  right -42px

.side-decoration.first
  top 0

.side-decoration.second
  bottom 5%
  left -40px

  @media (min-width: 1024px)
    left -56px

.side-decoration.third
  bottom 24%

.side-patron
  top 40%
  left -90px

  @media (min-width: 1024px)
    left -108px
</style>
