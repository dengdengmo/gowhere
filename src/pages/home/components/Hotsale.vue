<template>
  <div class="group">
    <div class="group-title">
      <img class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="">
      <span class="title">本周热门榜单</span> <!--这个元素与上一个元素之间有一个空格-->
      <a class="title-more" href="">
        全部榜单<svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-more"></use>
        </svg>
        </a>
    </div>
    <ul class="hotsale-list">
      <li class="hotsale-item" v-for="item of hotsaleList" :key="item.id">
        <div class="hotsale-tag" v-if="item.tagImgUrl">
          <img class="hotsale-tagimg" :src="item.tagImgUrl" alt="">
        </div>
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" :alt="item.desc" class="item-img">
        </div>
        <p class="hotsale-info">{{item.desc}}</p>
        <div class="hotsale-price">
          <span class="price">
            ￥<em class="price-num">{{item.price}}</em>
          </span>起
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeSale',
  props: {
    hotsaleList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
.group
  margin-top .2rem
  background #fff
  .group-title
    position relative
    padding .24rem 0 .26rem
    .title-img
      title-img()
    .title
      title()
    .title-more
      position absolute
      top .36rem
      right .32rem
      font-size .28rem
      color #616161
      line-height .28rem
      .icon
        font-size .35rem
  .hotsale-list
    display: flex
    overflow-x: scroll
    padding: 0 0.24rem
    .hotsale-item
      position relative
      padding: 0.06rem 0.02rem
      &:not(:first-child)
        margin-left .12rem
      .hotsale-tag
        position absolute
        top 0
        left 0
        z-index 1
        overflow hidden
        width .84rem
        height .4rem
        .hotsale-tagimg
          width 100%
      .item-img-wrapper
        width: 2rem
        // height: 0
        overflow hidden
        // padding-bottom 100%
        .item-img
          width 100%
      .hotsale-info
        margin-top .12rem
        color #212121
        font-size .24rem
        line-height .32rem
        text-align center
        ellipsis()
      .hotsale-price
        color #616161
        font-size .24rem
        line-height .36rem
        text-align center
        .price
          color $priceColor
          .price-num
            font-size .28rem
</style>
