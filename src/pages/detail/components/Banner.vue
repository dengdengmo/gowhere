<template>
  <div>
    <div class="banner">
      <div class="img-wrapper" @click="toggleGallery">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg" alt="">
      </div>
      <div class="banner-info">
        <div class="imgswiper">
          <svg class="icon" aria-hidden="true">
            <use xlink:href="#icon-tupian"></use>
          </svg>
          <em class="imgswiper-num">10</em>
        </div>
        <div class="banner-title">故宫(AAAAA景区)</div>
      </div>
    </div>
    <common-gallery :imgs="imgs"
     v-show="showGallery" @closeGallery="toggleGallery">
    </common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallery
  },
  data () {
    return {
      showGallery: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_r_800x800_6edd8174.jpg', 'http://img1.qunarzz.com/sight/p55/201211/04/fbcab3e5d6479ce893835fbb.jpg_r_800x800_6360f514.jpg']
    }
  },
  methods: {
    toggleGallery () {
      this.showGallery = !this.showGallery
    }
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position relative
  .img-wrapper
    overflow hidden
    height 0
    width 100%
    padding-bottom 55%
    .banner-img
      width 100%
  .banner-info
    position absolute
    left .2rem
    right .2rem
    bottom .36rem
    min-height .4rem
    color #ffffff
    .imgswiper
      width 1.2rem
      height .4rem
      line-height .4rem
      background rgba(0,0,0,.5)
      border-radius .2rem
      font-size .24rem
      text-align center
      margin-bottom .1rem
    .banner-title
      font-size .36rem
      line-height .4rem
  &::after
    content ''
    display block
    position absolute
    bottom 0
    left 0
    width 100%
    min-height .6rem
    background-color transparent
    background-image linear-gradient(to bottom, rgba(0,0,0,0), rgba(0,0,0,.8))
</style>
