<template>
  <section>
    <div>
      <h1>
        <small><span />We're still working<span /></small>
        Get Notified When We Launch
      </h1>
      <div class="input-container">
        <input type="email" placeholder="Enter Your Email Address" />
        <button>Notify Me</button>
      </div>
    </div>
    <img src="@/assets/images/hero.png" alt="Your Order has been picked up" />
    <div class="x" />
  </section>
</template>

<style lang="stylus" scoped>
text(size, spacing)
  font-size size
  margin spacing

item(bg, length, radius)
  background-color bg
  border-radius radius
  width length

section
  position relative

  @media (min-width: 768px)
    align-items center
    display grid
    grid-template-columns 1fr 1fr

h1
  font-size 2.8rem
  line-height 1.2
  width 25rem

  @media (min-width: 768px)
    font-size 3.2rem
    width 29rem

  @media (min-width: 1024px)
    font-size 4.2rem
    line-height 1.25
    width 38rem

  @media (min-width: 540px) and (max-width: 767px)
    width 32rem

  @media (max-width: 767px)
    margin 0 auto
    text-align center

small
  align-items center
  color #fbbb21
  display flex
  font-weight normal
  letter-spacing 0
  text(1.5rem, 2rem 0 1rem)

  @media (min-width: 768px)
    font-size 1.4rem
    margin-top 0

  @media (max-width: 767px)
    justify-content center

span
  display block
  height 0.3rem
  item(#fbbb21, 2.8rem, 0.4rem)
  margin 0 1rem

  @media (min-width: 768px)
    margin-left 0
    &:nth-of-type(2)
      display none

button
  color white
  font-weight bold
  item(#fbbb21, 12rem, 3.6rem)
  text-transform uppercase
  margin-left -2.6rem

  @media (min-width: 540px)
    margin-left -8rem

  @media (min-width: 1024px)
    margin-left -12rem
    width 15rem

input
  item(#eff3f4, 100%, 3.2rem 0 0 3.6rem)
  padding 1.6rem 3.2rem 1.6rem 2.6rem

  @media (min-width: 540px)
    padding 2rem 8.6rem 2rem 2.6rem

  @media (min-width: 1024px)
    padding 2.5rem 13rem 2.5rem 3rem

img
  position relative
  left 0.2rem

.input-container
  display flex
  max-width 300px
  text(1.1rem, 2rem auto 1.6rem)

  @media (min-width: 540px)
    max-width 90%
    text(1.2rem, 2.1rem auto 1.8rem)

  @media (min-width: 768px)
    margin 2.4rem 0

  @media (min-width: 1024px)
    min-width 390px
    width 80%

.x
  right -40px
  top 28%

  @media (max-width: 767px)
    display none
</style>
