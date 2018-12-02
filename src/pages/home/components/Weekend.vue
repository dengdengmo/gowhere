<template>
  <div class="group">
    <h2 class="group-title">周末去哪儿</h2>
    <ul class="product">
      <li class="product-item" v-for="item of weekendList" :key="item.id">
        <div class="product-imgcontainer">
          <img :src="item.imgUrl" alt="">
        </div>
        <div class="product-info">
          <p class="product-name">{{item.title}}</p>
          <p class="product-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
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
