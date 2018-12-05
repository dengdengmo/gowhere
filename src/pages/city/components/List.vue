<template>
  <div class="city-list" ref="wrapper">
    <div>
      <section class="area">
        <div class="top">
          <h2>当前城市</h2>
        </div>
        <ul class="list">
          <li>北京</li>
        </ul>
      </section>
      <section class="area">
        <div class="top">
          <h2>热门城市</h2>
        </div>
        <ul class="list">
          <li v-for="item of hotCities" :key="item.id">
            {{item.name}}
          </li>
        </ul>
      </section>
      <section class="area"
       v-for="(item, index) of cities"
       :key="index"
       :ref="index">
        <div class="top">
          <h2>{{index}}</h2>
        </div>
        <ul class="list">
          <li  v-for="innerItem of item" :key="innerItem.id">
            {{innerItem.name}}
          </li>
        </ul>
      </section>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    cities: Object,
    hotCities: Array,
    letter: String
  },
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  },
  watch: {
    letter () {
      if (this.letter) {
        const element = this.$refs[this.letter][0]
        this.scroll.scrollToElement(element)
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
@import '~styles/varibles.styl'
.city-list
  overflow hidden
  position absolute
  top 1.58rem
  left 0
  right 0
  bottom 0
  background #f5f5f5
  .top
    overflow hidden
    // position sticky
    // top 0
    // z-index 99
    h2
      font-size .24rem
      margin .24rem .3rem
  .list
    position relative
    overflow hidden
    background #fff
    display grid
    grid-template-columns  repeat(3, 1fr)
    &::before
      content ''
      position absolute
      width 33.3%
      height 100%
      left 33.3%
      border-left .02rem solid #dddddd
      border-right .02rem solid #dddddd
    li
      height .9rem
      line-height .9rem
      font-size .28rem
      text-align center
      border-bottom .02rem solid #dddddd
      margin-bottom -1px
      // z-index 20
</style>
