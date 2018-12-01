<template>
  <div class="main-page">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-hotsale></home-hotsale>
    <home-like></home-like>
    <home-weekend></home-weekend>
    <div class="price-desc">
      <span class="price-desc-icon"></span>
      <div class="price-desc-info">
        <span class="price-desc-highlight">票面价</span>
        是指通过景区指定窗口售卖的纸质门票上标注的价格
      </div>
    </div>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHotsale from './components/Hotsale'
import HomeLike from './components/Like'
import HomeWeekend from './components/Weekend'
export default {
  name: 'HelloWorld',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotsale,
    HomeLike,
    HomeWeekend
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.main-page
  background-color #f5f5f5
  .price-desc
    margin-top .1rem
    padding .14rem .1rem
    font-size .24rem
    line-height .32rem
    background #ffffff
    color #616161
    .price-desc-info
      margin-left .3rem
      .price-desc-highlight
        font-weight bold
</style>
