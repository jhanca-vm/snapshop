<template>
  <section>
    <div class="figures">
      <span class="side-patron" />
      <span class="side-decoration" />
      <b>About Us</b>
      <img src="@/assets/images/about-us-2.png" alt="" />
    </div>
    <div class="items">
      <article v-for="{ id, title, image, description } in items" :key="id">
        <figure>
          <img :src="require(`@/assets/images/${image}`)" :alt="title" />
        </figure>
        <div>
          <span class="line" />
          <h3>{{ title }}</h3>
          <p>{{ description }}</p>
        </div>
      </article>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import aboutData from '@/data/about.json'

export default defineComponent({
  name: 'Items',
  setup() {
    return { items: aboutData }
  },
})
</script>

<style lang="stylus" scoped>
side(down, aside)
  left aside
  top down

section
  @media (min-width: 768px)
    align-items center
    display grid
    grid-template-columns 1fr 1fr

  @media (min-width: 1024px)
    grid-template-columns 58% 42%
    margin-top -3.2rem

h3
  font-size 1.8rem
  margin 0.4rem 0

  @media (min-width: 540px)
    font-size 2.2rem

b
  color #ecf4fe
  font-size 9vw
  line-height 1
  writing-mode vertical-lr

  @media (max-width: 1023px) {
    display none
  }

article
  display flex

article img
  margin-right 28px
  width 60px

  @media (min-width: 540px)
    width 80px

  @media (min-width: 1024px)
    width 92px

p
  font-size 1.2rem

  @media (min-width: 540px)
    font-size 1.4rem

.figures
  position relative

  @media (min-width: 1024px)
    display grid
    grid-template-columns max-content 1fr

  @media (max-width: 767px)
    display none

.figures img
  @media (min-width: 1024px)
    left -10%
    position relative
    width 96%

.side-patron
  side(16%, -84px)

.side-decoration
  side(56%, -28px)

.items
  display grid
  padding 0 10px
  row-gap 3.6rem

  @media (min-width: 1024px)
    row-gap 6rem
</style>
