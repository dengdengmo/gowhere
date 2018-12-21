<template>
  <header>
    <router-link class="detail-back"
     tag="div" to="/" v-show="!showHeader">
      <div class="detail-back-icon">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-fanhui"></use>
        </svg>
      </div>
    </router-link>
    <div class="detail-header" v-show="showHeader" :style="opacityStyle">
      <router-link class="detail-back-left"
       tag="span" to="/">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-fanhui"></use>
        </svg>
      </router-link>
      <p class="detail-header-title">故宫</p>
    </div>
  </header>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showHeader: false,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleShowHeader () {
      const top = document.documentElement.scrollTop || window.pageYOffset
      if (top > 20) {
        let opacity = top / 140
        this.opacityStyle = { opacity }
        opacity = opacity > 1 ? 1 : opacity
        this.showHeader = true
      } else {
        this.showHeader = false
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleShowHeader)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleShowHeader)
  }
}
</script>

<style lang="stylus" scoped>
@import "~styles/varibles.styl";
@import "~styles/mixins.styl"
  header
    .detail-back
      position absolute
      top .1rem
      left .1rem
      width .72rem
      height .72rem
      line-height .72rem
      border-radius 50%
      background-color rgb(0, 0, 0)
      opacity .5
      text-align center
      .detail-back-icon
        color #fff
        // text-align center
        .icon
          font-size .45rem
          vertical-align -.12rem
    .detail-header
      position fixed
      top 0
      left 0
      right 0
      height $headerHeight
      line-height $headerHeight
      background-color $bgColor
      color #fff
      z-index 99
      .detail-back-left
        position absolute
        top 0
        left 0
        width .8rem
        height .8rem
        font-size .36rem
        text-align center
        .icon
          font-size .5rem
          vertical-align -.13rem
      .detail-header-title
        margin 0 .8rem
        font-size .32rem
        text-align center
        ellipsis()
</style>
