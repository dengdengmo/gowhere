<template>
  <section class="header">
    <div class="header-left">
    返回
    </div>
    <div class="header-input">
      输入城市/经典/游玩主题
    </div>
    <div class="header-right">
      城市
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl";
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
    .header-input
      background: #ffffff
      border-radius: .1rem
      flex: 1
      margin-top: .12rem
      height: .64rem
      line-height: .64rem
      margin-left: .2rem
      color: #ccc
    .header-right
      width: 1.24rem
      float: right
      text-align: center
</style>
