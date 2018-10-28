<template lang="pug">
  include ../../node_modules/bemto.pug/bemto.pug

  +b.mainslider
    +e.UL.list
      transition(name="current" appear)
        +e.LI.item_hongkong._current(key="0")
          +e.item-wrap
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
      transition(name="next" appear)
        +e.LI.item_prada._next(@click="toggleCurrentItem" key="1")
          +e.H2.item-title <span>Prada</span> Factory
          +e.item-img-wrap
            IMG(class="mainslider__item-img" src="/static/images/slide-2.jpg")
          +e.item-text-wrap
            +e.P.item-text Choosing An Antiaging Eye Cream
            +e.item-location
              +e.item-link(href="#") Magazyny
              +e.TIME.item-time(datetime="2017-05-08T00:06") 08 maja 2017, 00:06
</template>

<script>
export default {
  name: 'MainSlider',
  data() {
    return {
      nextItemIsShow: false,
    };
  },
  methods: {
    toggleCurrentItem(e) {
      const nextItem = e.currentTarget;
      const currentItem = document.querySelector('.mainslider__item_current');

      if (!this.nextItemIsShow) {
        currentItem.style.transform = 'translateX(-270px)';
        nextItem.style.transform = 'translateX(-270px)';
        this.nextItemIsShow = true;
      } else {
        currentItem.style.transform = 'translateX(0)';
        nextItem.style.transform = 'translateX(0)';
        this.nextItemIsShow = false;
      }
    },
  },
};
</script>

<style lang="stylus" scoped>
  .mainslider

    &__list
      display flex
      position relative
      width 100%
      height 850px
      overflow hidden

    &__item
      top 0
      height 100%
      position absolute
      color #fff
      transition 1s

      &_current
        width 100%
        left 0

      &_next
        width 520px
        right -220px
        flex-direction column
        align-items center
        padding-left 130px
        transition all 1s

        &:hover
          transform scale(1.05)

    &__item-wrap
      position relative
      width 100%
      height 100%

    &__item_hongkong &__item-text-wrap
      position absolute
      bottom 120px
      left 110px
      height 225px
      transform rotate(-90deg) translateY(100%)
      transform-origin bottom left

    &__item_hongkong &__item-promo-title
      display block
      margin-bottom 30px
      padding-left 180px
      font-size 72px
      font-weight 400

    &__item_hongkong &__item-title
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
      position absolute
      top 70px
      left 50%
      transform translateX(-50%)

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
      font-weight 400
      color #000
      font-size 72px

      & span
        display block
        padding-left 190px

    &__item_prada &__item-img-wrap
      margin-bottom 35px
      padding-top 135px

    &__item_prada &__item-text-wrap
      width 300px

    &__item_prada &__item-text
      margin-bottom 5px
      font-size 28px
      line-height 42px
      text-align center

    &__item_prada &__item-location
      display flex
      justify-content center

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


    .current-enter
      transform translateX(-5000px)

    .current-enter-to
      transform translateX(0)

    .current-enter, .current-enter-to
      transition 1.6s

    .next-enter
      transform translateX(-5000px)

    .next-enter-to
      transform translateX(0)

    .next-enter, .next-enter-to
      transition 1s
</style>
