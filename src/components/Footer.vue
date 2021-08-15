<template>
  <footer>
    <div>
      <p>Follow Us</p>
      <a href="#"><span class="facebook" /></a>
      <a href="#"><span class="instagram" /></a>
      <a href="#"><span class="linkedin" /></a>
    </div>
    <nav>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#how-it-works">How it Works</a></li>
        <li><a href="#">Privacy Policy</a></li>
      </ul>
    </nav>
  </footer>
</template>

<style lang="stylus" scoped>
icon(name)
  background url('~@/assets/images/' + name + '.svg') no-repeat center
  background-size contain
  display inline-block
  height 2rem
  width 2rem

footer
  font-size 1.3rem
  margin 0 32px
  padding 2rem 0
  text-align center

  @media (min-width: 540px)
    margin 0 60px

  @media (min-width: 640px)
    align-items flex-end
    background url('~@/assets/images/circles.svg') no-repeat
    background-position-x -30%
    background-size 52%
    display grid
    grid-template-columns 1fr 1fr
    margin 0
    padding 8rem 60px 2.4rem

  @media (min-width: 768px)
    background-position-x -28%
    background-size 48%
    padding-top 12rem

  @media (min-width: 1024px)
    background-position-x -14%
    background-size 34%
    padding 12rem 80px 3.2rem

  @media (max-width: 540px)
    border-top 1px solid #171717

div
  @media (min-width: 640px)
    text-align left

ul
  display flex
  justify-content space-between
  list-style none
  margin-top 2rem

  @media (min-width: 1024px)
    margin-left auto
    max-width 350px

a
  color inherit
  text-decoration none

.facebook
  icon('facebook')

.instagram
  icon('instagram')
  margin 1rem 4.6rem 0 4rem

  @media (min-width: 640px)
    margin 1rem 1.6rem 0 1rem

.linkedin
  icon('linkedin')
</style>
