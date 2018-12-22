<template>
  <div class="main-page">
    <home-header></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconList="iconList"></home-icons>
    <home-hotsale :hotsaleList="hotsaleList"></home-hotsale>
    <home-recommend :likeList="recommendList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
    <div class="price-desc">
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-tishi"></use>
      </svg>
      <div class="price-desc-info">
        <span class="price-desc-highlight">票面价</span>
        是指通过景区指定窗口售卖的纸质门票上标注的价格
      </div>
    </div>
    <qunar-footer></qunar-footer>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeHotsale from './components/Hotsale'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import QunarFooter from 'common/Footer'
import axios from 'axios'
import { mapState } from 'vuex'
export default {
  name: 'HelloWorld',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeHotsale,
    HomeRecommend,
    HomeWeekend,
    QunarFooter
  },
  data () {
    return {
      hotsaleList: [],
      recommendList: [],
      swiperList: [],
      iconList: [],
      weekendList: [],
      lastCity: ''
    }
  },
  computed: {
    ...mapState(['city'])
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.hotsaleList = data.hotsaleList
        this.recommendList = data.recommendList
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.weekendList = data.weekendList
        sessionStorage.recommendList = JSON.stringify(data.recommendList)
      }
    }
  },
  mounted () {
    this.lastCity = this.city
    this.getHomeInfo()
  },
  activated () {
    if (this.lastCity !== this.city) {
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
.main-page
  background-color #f5f5f5
  .price-desc
    position relative
    margin-top .1rem
    padding .14rem .1rem
    font-size .24rem
    line-height .32rem
    background #ffffff
    color #616161
    .icon
      position absolute
      left 6px
      bottom 10px
      color #ccc
    .price-desc-info
      margin-left .3rem
      .price-desc-highlight
        font-weight bold
</style>
