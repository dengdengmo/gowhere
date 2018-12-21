<template>
  <div class="group">
    <h3 class="group-title border-bottom">看了该景点的人还看了</h3>
    <ul class="like-list">
      <router-link tag="li"
       class="like-item border-bottom"
        v-for="item of likeList" :key="item.id"
        :to="'/detail/' + item.id">
        <div class="like-imgcon">
          <img :src="item.imgUrl" :alt="item.title" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">{{item.title}}</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="item.score"></star>
            <span class="comment-num">{{item.commentNum}}条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">{{item.price}}</em>
            </span>
            起
            <span class="like-address">{{item.address}}</span>
          </div>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
import star from 'common/star/star'
export default {
  name: 'HomeLike',
  data () {
    return {
      likeList: JSON.parse(sessionStorage.recommendList)
    }
  },
  components: {
    star
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
    margin-bottom -.02rem
    padding 0 .2rem
    height .88rem
    line-height .88rem
    fangt-size .3rem
    background-color #ffffff
    color #333
    text-indent .2rem
    &::after
      content ''
      position absolute
      top .3rem
      left .2rem
      width .06rem
      height .25rem
      background-color #1ba9ba
  .like-list
    margin-left .24rem
    .like-item
      overflow hidden
      padding .2rem 0
      .like-imgcon
        float left
        overflow hidden
        width 2rem
        height 2rem
        .like-img
          width 100%
      .like-info
        overflow hidden
        padding-left .22rem
        .like-title
          margin-top .26rem
          color #212121
          font-size .32rem
          height .44rem
          line-height .44rem
        .like-comment
          margin-top .14rem
          height .34rem
          font-size 0
          .star-level
            display inline-block
            position relative
            width 1.7rem
            height .28rem
            line-height .28rem
            transform scale(1.16)
            transform-origin left
          .comment-num
            color #616161
            font-size .24rem
            line-height .34rem
        .like-price
          margin-top .22rem
          position relative
          color #616161
          font-size .24rem
          line-height .4rem
          .price
            color $priceColor
            .price-num
              font-size .4rem
          .like-address
            position absolute
            right .24rem
</style>
