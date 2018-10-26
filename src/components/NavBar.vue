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
    +e.btn_like(href="#")
    +e.NAV.links_left
      +e.UL.links-list
        +e.links-item
          +e.links-link(href="#") News
        +e.links-item
          +e.links-link(href="#") Fashion
        +e.links-item
          +e.links-link(href="#") Living
    +e.mainlogo(href="#" aria-label="Wmagazine")
    +e.NAV.links_right
      +e.UL.links-list
        +e.links-item
          +e.links-link(href="#") Tech
        +e.links-item
          +e.links-link(href="#") Media
        +e.links-item
          +e.links-link(href="#") Covers
    +e.btn_subscribe(href="#") Subscribe
    +e.INPUT.search
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

</style>
