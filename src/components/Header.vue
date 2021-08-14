<template>
  <header>
    <span />
    <figure>
      <img src="@/assets/images/logo.svg" alt="snapshop logo" />
      <figcaption>SnapShop</figcaption>
    </figure>
  </header>
</template>

<style lang="stylus" scoped>
move-to(prop, args)
  display block
  position relative
  {prop} args

header
  padding 0 40px

  @media (min-width: 540px)
    padding 0 60px

  @media (min-width: 1024px)
    padding 0 80px

span
  background url('~@/assets/images/header-decoration.svg') no-repeat
  background-size contain
  height 3.75rem
  margin 0 0 1.2rem 1.8rem
  move-to('top', -0.05rem)
  width 20rem

  @media (min-width: 540px)
    margin 0 0 0 auto
    right 16%

  @media (min-width: 1024px)
    right 24%

figure
  color #0d72fa
  font-size 2.4rem
  font-weight bold

  @media (min-width: 540px)
    font-size 2.2rem
    margin-top -0.8rem
    width fit-content

img
  display none

  @media (min-width: 540px)
    margin 0 auto -0.4rem
    move-to('right', 0.8rem)
    width 4.8rem
</style>
