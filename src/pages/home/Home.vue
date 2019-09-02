<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import HomeHeader from './components/Header'
// eslint-disable-next-line no-unused-vars
import HomeSwiper from './components/Swiper'
// eslint-disable-next-line no-unused-vars
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {
    HomeRecommend,
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeWeekend
  }
}
</script>

<style>
</style>
