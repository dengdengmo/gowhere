<template>
  <div class="ticket-tabs border-bottom" :class="{'tab-fixed': fixed}" ref="ticketTab">
    <div class="tab-container" @click="toAnchor">
      <span class="tabitem" data-anchor="anchor_1">门票</span>
      <span class="tabitem" data-anchor="anchor_2">一日游</span>
      <span class="tabitem" data-anchor="anchor_3">热销组合</span>
      <span class="tabitem" data-anchor="anchor_4">景区服务</span>
    </div>
    <span class="tab-slider" :style="{left: left + 'px'}"></span>
  </div>
</template>

<script>
export default {
  name: 'TicketTab',
  data () {
    return {
      fixed: false,
      num: 0
    }
  },
  computed: {
    top: function () {
      return this.$refs.ticketTab.offsetTop - 86
    },
    height: function () {
      return document.querySelector('.ticket-container').offsetHeight + 100
    },
    left: function () {
      return this.num + 15
    }
  },
  methods: {
    fixTab () {
      // eslint-disable-next-line one-var
      const scrollTop = document.documentElement.scrollTop || window.pageYOffset
      if (scrollTop >= this.top && scrollTop < this.height) {
        this.fixed = true
      } else {
        this.fixed = false
      }
    },
    toAnchor (e) {
      let anchor = e.target.getAttribute('data-anchor')
      let el = document.querySelector('#' + anchor)
      const num = el.getAttribute('data-anchor')
      this.num = (num - 1) * 95
      el.scrollIntoView({
        behavior: 'smooth',
        block: 'center',
        inline: 'nearest'
      })
    }
  },
  activated () {
    window.addEventListener('scroll', this.fixTab)
  },
  deactivated () {
    window.removeEventListener('scroll', this.fixTab)
  }
}
</script>

<style lang="stylus" scoped>
.ticket-tabs
  position relative
  background #ffffff
  color #212121
  height .96rem
  line-height .96rem
  white-space nowrap
  .tab-container
    width 8.2rem
    .tabitem
      display inline-block
      height .92rem
      width 1.85rem
      font-size .32rem
      text-align center
  .tab-slider
    position absolute
    bottom 0
    left 15px
    display inline-block
    width 1.4rem
    height .04rem
    background-color #00bcd4
.tab-fixed
  position fixed
  top .86rem
  z-index 99
</style>
