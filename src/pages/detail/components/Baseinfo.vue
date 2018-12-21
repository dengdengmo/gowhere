<template>
  <div class="baseinfo">
    <div class="flex-card border-bottom">
      <div class="flex-item">
        <div class="comment">
          <span class="comment-score">5.0</span>
          <span class="comment-text">分</span>
          <span class="comment-desc">超赞</span>
        </div>
        <div class="comment-num">
          <span class="num">337423条评论</span>
          <span class="num">90条攻略</span>
          <svg class="icon icon-left" aria-hidden="true">
            <use xlink:href="#icon-more"></use>
          </svg>
        </div>
      </div>
      <div class="flex-item border-left">
        <div>
          <span class="sight-card-title">景点简介</span>
        </div>
        <div>
          <span class="sight-card-text">开放时间、贴士</span> <!--不放在span标签里就会有一个像素的高度差 -->
        </div>
        <svg class="icon icon-right" aria-hidden="true">
          <use xlink:href="#icon-more"></use>
        </svg>
      </div>
    </div>
    <div class="sight-address">
      <p>
        <svg class="icon icon-left" aria-hidden="true">
          <use xlink:href="#icon-tishi"></use>
        </svg>
        <span class="sight-address-text">北京市东城区景山前街4号</span>
        <svg class="icon icon-right" aria-hidden="true">
          <use xlink:href="#icon-more"></use>
        </svg>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBaseinfo'
}
</script>

<style lang="stylus" scoped>
@import "~styles/varibles.styl"
@import "~styles/mixins.styl"
.baseinfo
  position relative
  top -.1rem
  padding .1rem .2rem 0 .2rem
  margin-bottom .1rem
  background #fff
  border-radius .1rem .1rem 0 0
  .flex-card
    padding-top .1rem
    padding-bottom .2rem
    display flex
    width 100%
    .flex-item
      position relative
      flex 1
      .comment
        color $priceColor
        font-size 0
        .comment-score
          font-size .44rem
          line-height .44rem
        .comment-text
          font-size .28rem
          line-height .48rem
        .comment-desc
          font-size .28rem
          line-height .48rem
          margin-left .2rem
      .comment-num
        .num
          font-size .24rem
          color #9e9e9e
          margin-right .2rem
        .icon-left
          position absolute
          top .2rem
          right .1rem
          color #9e9e9e
          font-size .4rem
      .icon-right
        position absolute
        top .2rem
        right 0
        color #9e9e9e
        font-size .4rem
      .sight-card-title
        font-size .28rem
        color #212121
        line-height .48rem
        padding-left .3rem
      .sight-card-text
        font-size .24rem
        color #9e9e9e
        padding-left .3rem
  .sight-address
    position relative
    color #212121
    padding .2rem 0
    line-height .36rem
    p
      padding 0 .56rem
      position relative
      .icon-left
        position absolute
        left 0
        color #9e9e9e
        font-size .36rem
      .icon-right
        position absolute
        right 0
        color #9e9e9e
        font-size .4rem

</style>
