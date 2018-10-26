<template lang="pug">
  include ../../node_modules/bemto.pug/bemto.pug

  +b.mainslider
    +e.UL.list
      +e.LI.item_hong-kong
        +e.H2.item-title Opens with Show
        +e.H3.item-subtitle Hong Kong Fashion Week
        +e.item-links-wrap
          +e.item-link(href="#") Producing Perfume From Home
          +e.item-link(href="#") The 10 Commandments
        +e.item-img-wrap
          IMG(class="mainslider__item-img")
      +e.LI.item_prada
        +e.H2.item-title Prada
        +e.H2.item-subtitle Factory
        +e.P.item-text
        +e.item-location
          +e.item-link(href="#") Magazyny
          +e.TIME.item-link(datetime="2017-05-08T00:06") 08 maja 2017, 00:06
        +e.item-img-wrap
          IMG(class="mainslider__item-img")
</template>

<script>
export default {
  name: 'MainSlider',
};
</script>

<style lang="stylus" scoped>

</style>
