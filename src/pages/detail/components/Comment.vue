<template>
  <div class="comment-container">
    <h3 class="comment-title border-bottom">用户评论</h3>
    <div class="comment-list">
      <comment-item></comment-item>
      <comment-item></comment-item>
    </div>
    <div class="comment-more border-top">
      查看全部评论<svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-more"></use>
      </svg>
    </div>
  </div>
</template>

<script>
import commentItem from './commentItem'
export default {
  name: 'DetailComment',
  components: {
    commentItem
  }
}
</script>

<style lang="stylus" scoped>
.comment-container
  margin-top .2rem
  .comment-title
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
  .comment-list
    background #fff
  .comment-more
    height .8rem
    line-height .8rem
    background #fff
    text-align center
    .icon
      margin-left .05rem
      font-size .3rem
      color #616161
</style>
