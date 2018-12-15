<template>
  <div class="main-page">
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-baseinfo></detail-baseinfo>
    <div class="content"></div>
  </div>
</template>

<script>
import detailBanner from './components/Banner'
import detailHeader from './components/Header'
import detailBaseinfo from './components/Baseinfo'
export default {
  name: 'Detail',
  components: {
    detailBanner,
    detailHeader,
    detailBaseinfo
  }
}
</script>

<style lang="stylus" scoped>
.main-page
  background #f5f5f5
  .content
    height 50rem
</style>
