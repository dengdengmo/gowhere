<template>
  <ul class="list">
    <li class="item"
       v-for="(item, index) of cities"
       :key="index" >
      {{index}}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
.list
  display flex
  flex-direction column
  justify-content center
  position absolute
  top 1.58rem
  right 0
  bottom 0
  width .4rem
  // z-index 100
  .item
    line-height .3rem
    text-align center
    color #00bcd4
    font-size .2rem
</style>
