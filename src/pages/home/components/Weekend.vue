<template>
  <div class="group">
    <h2 class="group-title">周末去哪儿</h2>
    <ul class="product">
      <li class="product-item">
        <div class="product-imgcontainer">
          <img src="http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">京城人的周末撒欢地</p>
          <p class="product-desc">在帝都过周末，不仅仅是城中游</p>
        </div>
      </li>
      <li class="product-item">
        <div class="product-imgcontainer">
          <img src="http://img1.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">京城欢乐亲子游</p>
          <p class="product-desc">德智体美劳全面发展的亲子日，这些地方因该去看看...</p>
        </div>
      </li>
      <li class="product-item">
        <div class="product-imgcontainer">
          <img src="http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">京城有好泉</p>
          <p class="product-desc">细数北京温泉，温暖你的冬天</p>
        </div>
      </li>
      <li class="product-item">
        <div class="product-imgcontainer">
          <img src="http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">北京必游TOP10</p>
          <p class="product-desc">来北京必去的景点非这些地方莫属</p>
        </div>
      </li>
      <li class="product-item">
        <div class="product-imgcontainer">
          <img src="http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">寻找北京的皇城范儿</p>
          <p class="product-desc">数百年的宫廷庙宇，至今依旧威严霸气</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend'
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.group
  .group-title
    height .8rem
    line-height .8rem
    padding-left .26rem
    color #212121
  .product
    .product-item
      position relative
      margin-bottom .1rem
      background #fff
      .product-imgcontainer
        overflow hidden
        height 0
        padding-bottom 37.4375%
        img
          width 100%
      .product-info
        position relative
        padding .14rem .2rem .2rem .2rem
        .product-name
          color #212121
          font-size .28rem
          line-height .48rem
          padding-right 1.4rem
          ellipsis()
        .product-desc
          color #616161
          font-size .24rem
          line-height .42rem
          padding-right 1.4rem
          ellipsis()
</style>
