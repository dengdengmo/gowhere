<template>
  <div class="ticket-group">
    <h3 class="ticket-group-title border-bottom">
      <span class="title-bgimg"></span>故宫当日票
    </h3>
    <ticket-list></ticket-list>
    <ticket-list></ticket-list>
    <div class="more-btn border-bottom" @click="extendMore" v-show="hideTicket">
      查看剩余产品
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-jiantou-xia"></use>
      </svg>
    </div>
  </div>
</template>

<script>
import ticketList from './TicketList'
export default {
  name: 'TicketGroup',
  data () {
    return {
      hideTicket: true
    }
  },
  components: {
    ticketList
  },
  methods: {
    extendMore () {
      this.hideTicket = false
    }
  }
}
</script>

<style lang="stylus" scoped>
.ticket-group
  background #ffffff
  margin-bottom .2rem
  .ticket-group-title
    overflow hidden
    position relative
    height .88rem
    line-height .88rem
    padding 0 .2rem
    font-size .32rem
    color #333
    background #fff
    text-indent .4rem
    .title-bgimg
      position absolute
      display inline-block
      width .36rem
      height .36rem
      top .26rem
      left .2rem
      margin-right .1rem
      background url('//s.qunarzz.com/piao/image/touch/sight/detail.png') 0 -.45rem no-repeat
      background-size .4rem 3rem
  .more-btn
    position relative
    height .8rem
    line-height .8rem
    color #616161
    text-align center
</style>
