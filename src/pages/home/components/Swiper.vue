/* eslint-disable vue/no-parsing-error */
<template>
  <section class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </section>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true,
        observer: true,
        observeParents: true,
        autoplay: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiperList.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullets
    bottom 6px
    .swiper-pagination-bullet-active
      background #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 27%
    background #ccc
    .swiper-img
      width: 100%
</style>
