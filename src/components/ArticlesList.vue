<template lang="pug">
  include ../../node_modules/bemto.pug/bemto.pug

  +b.UL.article-list
    +e.LI.item
      +e.item-wrap
        +e.item-text-wrap
          +e.H3.item-title Breast Enlargement Exercises Cheapest Inborn Sense Promoting
          +e.TIME.item-date(datetime="2018-05-17") 17 May 2018
        IMG(class="article-list__item-img" src="/static/images/article-1.jpg")
    +e.LI.item
      +e.item-wrap
        +e.item-text-wrap
          +e.H3.item-title Sensible Beauty Tips For Enhancing Your Appearance
          +e.TIME.item-date(datetime="2018-07-29") 29 Jul 2018
        img(class="article-list__item-img" src="/static/images/article-2.jpg")
    +e.LI.item
      +e.item-wrap
        +e.item-text-wrap
          +e.H3.item-title Proven Techniques Help You Herbal Breast Enlargement Guaranteed
          +e.TIME.item-date(datetime="2018-06-02") 02 Jun 2018
        img(class="article-list__item-img" src="/static/images/article-3.jpg")
    +e.LI.item
      +e.item-wrap
        +e.item-text-wrap
          +e.H3.item-title How To Save Money On Beauty Products
          +e.TIME.item-date(datetime="2018-02-13") 13 Feb 2018
        img(class="article-list__item-img" src="/static/images/article-4.jpg")
</template>

<script>
export default {
  name: 'ArticlesList',
};
</script>

<style lang="stylus" scoped>
  .article-list
    display flex
    justify-content center
    flex-wrap wrap
    margin 0
    padding 0
    list-style-type none
    background-color #000
    color #fff

    &__item
      width 250px
      padding 20px

    &__item:not(:last-child) &__item-wrap
      border-right 1px solid rgba(67, 70, 94, 0.66)

    &__item-wrap
      display flex
      flex-wrap wrap
      height 100%

    &__item-text-wrap
      width 170px

    &__item-title
      margin 0
      font-size 12px
      line-height 15px
      font-weight 400

    &__item-date
      color #67697C
      font-size 10px
      line-height 14px

    &__item-img
      width 40px
      height 40px

</style>
