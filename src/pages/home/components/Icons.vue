<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img-container">
            <img class="icon-img" :src="item.imgUrl" alt="">
          </div>
          <p class="keywords">{{item.keywords}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        keywords: '景点门票'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        keywords: '北京必游'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        keywords: '一日游'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        keywords: '文化古迹'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        keywords: '动植物园'
      }, {
        id: '0006',
        imgUrl: 'https://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        keywords: '打卡圣地'
      }, {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
        keywords: '野生动物园'
      }, {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
        keywords: '泡温泉'
      }, {
        id: '0009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
        keywords: '全部游玩'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    background-color #fff
    padding-bottom .2rem
    .icon
      position relative
      overflow hidden
      float left
      width 25%
      height 0
      padding-bottom 25%
      .icon-img-container
        position absolute
        top 0
        left 0
        right 0
        bottom .3rem
        box-sizing border-box
        padding .1rem
        .icon-img
          display block
          height 100%
          margin 0 auto
      .keywords
        position absolute
        left 0
        right 0
        bottom 0
        height .3rem
        line-height .3rem
        color $darkColor
        text-align center
        ellipsis()
</style>
