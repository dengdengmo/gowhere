<template>
  <div class="header">
    <a href="" class="backIcon">?</a>
    <div class="header-title">城市选择</div>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
@import '~styles/varibles.styl'
.header
  position relative
  background #00bcd4
  .backIcon
    position absolute
    left 0
    top 0
    width .8rem
    height .88rem
    line-height .88rem
    font-size .36rem
    text-align center
    color #fff
  .header-title
    margin 0 1rem
    line-height .88rem
    color #ffffff
    font-size .32rem
    text-align center
    ellipsis()
</style>
