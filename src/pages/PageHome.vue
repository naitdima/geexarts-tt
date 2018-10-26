<template lang="pug">
  include ../../node_modules/bemto.pug/bemto.pug

  +b.SECTION.page-home
    NavBar(class="page-home__navbar")
    MainSlider(class="page-home__mainslider")
    ArticlesList(class="page-home__articles-list")
</template>

<script>
import NavBar from '@/components/NavBar';
import MainSlider from '@/components/MainSlider';
import ArticlesList from '@/components/ArticlesList';

export default {
  name: 'PageHome',
  components: {
    NavBar,
    MainSlider,
    ArticlesList,
  },
};
</script>

<style lang="stylus" scoped>

</style>
