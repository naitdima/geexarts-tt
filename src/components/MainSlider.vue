<template lang="pug">
  include ../../node_modules/bemto.pug/bemto.pug

  +b.mainslider
    +e.UL.list
      +e.LI.item_hongkong
        +e.item-text-wrap
          +e.B.item-promo-title Opens with Show
          +e.H2.item-title Hong Kong Fashion Week
          +e.item-links-wrap
            +e.item-link(href="#") Producing Perfume From Home
            +e.item-link(href="#") The 10 Commandments
        +e.item-img-wrap
          IMG(class="mainslider__item-img" src="/static/images/slide-1.jpg")
          +e.item-img-ball
          +e.item-img-text
      +e.LI.item_prada
        +e.H2.item-title <span>Prada</span> Factory
        +e.item-img-wrap
          IMG(class="mainslider__item-img" src="/static/images/slide-2.jpg")
        +e.P.item-text Choosing An Antiaging Eye Cream
        +e.item-location
          +e.item-link(href="#") Magazyny
          +e.TIME.item-time(datetime="2017-05-08T00:06") 08 maja 2017, 00:06
</template>

<script>
export default {
  name: 'MainSlider',
};
</script>

<style lang="stylus" scoped>
  .mainslider

    &__list
      display flex
      position relative
      width 100%
      height 850px
      overflow-x scroll
      margin 0
      padding 0
      padding-left 110px
      list-style-type none

    &__item
      position relative
      color #fff

      &_hongkong
        display flex
        margin-right 125px
        padding-left 340px

      &_prada
        display flex
        flex-direction column
        align-items center
        padding-left 130px

    &__item_hongkong &__item-text-wrap
      position absolute
      bottom 60px
      left 0
      height 225px
      // max-width 300px
      transform rotate(-90deg) translateY(100%)
      transform-origin bottom left

    &__item_hongkong &__item-promo-title
      display block
      margin-bottom 30px
      padding-left 180px
      font-size 72px
      font-weight 400

    &__item_hongkong &__item-title
      margin 0
      margin-bottom 45px
      color #4C4C4C
      font-size 56px
      line-height 64px

    &__item_hongkong &__item-links-wrap
      display flex
      align-items center
      padding-left 130px

    &__item_hongkong &__item-link
      display flex
      padding-left 20px
      padding-right 20px
      color #fff
      font-size 12px
      line-height 15px
      text-decoration none
      clip rect(auto, auto, auto, auto)

      &:not(:last-child)
        border-right 1px solid rgba(107, 107, 107, 0.42)

    &__item_hongkong &__item-img-wrap
      position relative
      margin-top 70px

    &__item_hongkong &__item-img-ball
      position absolute
      top 0
      left 50%
      transform translateX(-50%)
      width 490px
      height 490px
      border-radius 50%
      background-color #E4749D
      mask url(/static/images/mask-ball.svg)

    &__item_prada &__item-title
      position absolute
      top 70px
      left 0
      margin 0
      font-weight 400
      color #000
      font-size 72px

      & span
        display block
        padding-left 190px

    &__item_prada &__item-img-wrap
      margin-bottom 35px
      padding-top 135px

    &__item_prada &__item-text
      margin 0
      margin-bottom 5px
      font-size 28px
      line-height 42px
      text-align center

    &__item_prada &__item-location
      display flex

    &__item_prada &__item-link
      position relative
      margin-right 10px
      padding-right 7px
      opacity 0.8
      color #fff
      font-size 10px
      line-height 31px
      text-decoration none
      text-transform uppercase

      &::before
        position absolute
        content ''
        top 50%
        right 0
        transform translateY(-50%)
        width 3px
        height 3px
        background-color #fff
        opacity 0.3
        border-radius 50%

    &__item_prada &__item-time
      opacity 0.4
      font-size 10px
      line-height 31px
      text-transform uppercase
</style>
