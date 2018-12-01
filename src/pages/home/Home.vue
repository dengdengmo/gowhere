<template>
  <div class="main-page">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hotsale></home-hotsale>
    <home-like></home-like>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHotsale from './components/Hotsale'
import HomeLike from './components/Like'
export default {
  name: 'HelloWorld',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotsale,
    HomeLike
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.main-page
  background-color #f5f5f5
</style>
