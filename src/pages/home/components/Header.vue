<template>
  <section class="header">
    <div class="header-left">
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-fanhui"></use>
      </svg>
    </div>
    <div class="header-input">
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-sousuo"></use>
      </svg>
      输入城市/经典/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}<svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-xiajiantou"></use>
        </svg>
      </div>
    </router-link>
  </section>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl";
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      text-align center
      .icon
        color #fff
        font-size .5rem
        vertical-align -.17rem
    .header-input
      background: #ffffff
      border-radius: .1rem
      flex: 1
      margin-top: .12rem
      height: .64rem
      line-height: .64rem
      margin-left: .2rem
      color: #e4e7ea
      .icon
        font-size .33rem
        margin-left .2rem
        vertical-align -.05rem
    .header-right
      min-width: 1.04rem
      padding 0 .1rem
      float: right
      text-align: center
      color #fff
</style>
