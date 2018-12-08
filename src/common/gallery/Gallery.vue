<template>
  <div class="gallery" @click="closeGallery">
    <div class="imgs-wrapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="(item,key) of imgs" :key="key" :imgs="imgs">
          <img class="swiper-img" :src="item" alt="">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallery',
  props: {
    imgs: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
        // loop: true,
        observer: true,
        observeParents: true
      }
    }
  },
  methods: {
    closeGallery () {
      this.$emit('closeGallery')
    }
  }
}
</script>

<style lang="stylus" scoped>
.gallery >>> .swiper-container
  overflow inherit
.gallery
  position absolute
  display flex
  flex-direction column
  justify-content center
  top 0
  left 0
  right 0
  bottom 0
  background #000
  z-index 99
  .imgs-wrapper
    // overflow hidden
    height 0
    width 100%
    padding-bottom 100%
    .swiper-img
      width 100%
    .swiper-pagination
      color #fff
      bottom -4rem
      // z-index 100
</style>
