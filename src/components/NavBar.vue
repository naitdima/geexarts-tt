<template lang="pug">
  include ../../node_modules/bemto.pug/bemto.pug

  +b.SECTION.navbar
    +e.NAV.dropmenu
      +e.BUTTON.dropmenu-btn Sections
      +e.UL.dropmenu-list
        +e.dropmenu-item(
          v-for="(item, index) in sectionsList"
          :item="item"
          :key="index") {{ item }}
    +e.btn_like(href="#") Like us
    +e.NAV.links_left
      +e.UL.links-list
        +e.links-item
          +e.links-link(href="#") News
        +e.links-item
          +e.links-link(href="#") Fashion
        +e.links-item
          +e.links-link(href="#") Living
    +e.A.mainlogo Wmagazine
    +e.NAV.links_right
      +e.UL.links-list
        +e.links-item
          +e.links-link(href="#") Tech
        +e.links-item
          +e.links-link(href="#") Media
        +e.links-item
          +e.links-link(href="#") Covers
    +e.btn_subscribe(href="#") Subscribe
    +e.search-wrap
      +e.LABEL.search-label(for="search")
      +e.INPUT.search-input(type="search" id="search" method="get")
    +e.login(href="#")
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      sectionsList: ['Section 1', 'Section 2', 'Section 3', 'Section 4', 'Section 5', 'Section 6'],
    };
  },
};
</script>

<style lang="stylus" scoped>
  .navbar
    display flex
    flex-wrap wrap
    align-items center
    justify-content center
    padding-left 100px
    padding-right 100px
    padding-top 45px
    color white

    &__dropmenu
      margin-right 15px

    &__dropmenu-btn
      position relative
      padding-top 10px
      padding-bottom 10px
      padding-left 45px
      padding-right 20px
      text-transform uppercase
      background-color transparent
      color #fff
      font-size 10px
      line-height 14px
      border 1px solid rgba(255, 255, 255, 0.27)
      border-radius 4px

      &::before
      &::after
        position absolute
        content ''
        left 20px
        width 10px
        height 1px
        background-color #fff

      &::before
        top 15px

      &::after
        bottom 13px

    &__dropmenu-list
      display none

    &__btn
      display block
      flex 1
      position relative
      margin-right 40px
      padding-top 10px
      padding-bottom 10px
      padding-left 45px
      padding-right 10px
      background-color rgba(255, 255, 255, 0.08)
      border-radius 4px
      font-size 10px
      line-height 14px
      color #fff
      text-decoration none
      text-transform uppercase

      &::before
        position absolute
        content ''
        top 10px
        left 20px
        width 12px
        height 12px

    &__btn_like
      width 90px

      &::before
        background-image url("/static/images/like.svg")
        background-size cover

    &__btn_subscribe
      width 100px

      &::before
        background-image url("/static/images/subscribe.svg")
        background-size cover

    &__links
      display flex
      align-items center
      margin-right 30px

    &__links-list
      margin 0
      padding 0
      list-style-type none
      display flex
      flex-wrap wrap
      width 170px

    &__links-item:not(:last-child)
      margin-right 20px

    &__links-link
      color #fff
      font-size 15px
      line-height 18px
      text-decoration none

    &__mainlogo
      margin-right 100px
      color #fff
      font-size 42px
      line-height 56px

    &__search-wrap
      display flex
      align-items center
      margin-right 20px

    &__search-label
      width 15px
      height 15px
      background-image url("/static/images/search.svg")

    &__search-input
      display none

    &__login
      width 35px
      height 35px
      border-radius 50%
      background-image url("/static/images/user.png")
      background-size cover

</style>
