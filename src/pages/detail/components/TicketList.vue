<template>
  <div class="ticket-list border-bottom">
    <div class="ticket-list-info" @click="toggleTicketItem">
      <h5 class="ticket-name">上午场</h5>
      <div class="ticket-price">
        ￥<em class="price-num">40</em><span class="price-numword">起</span>
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-jiantou-xia" v-show="!showTicket"></use>
          <use xlink:href="#icon-jiantou-shang" v-show="showTicket"></use>
        </svg>
      </div>
    </div>
    <ticket-item v-show="showTicket"></ticket-item>
    <ticket-item v-show="showTicket"></ticket-item>
  </div>
</template>

<script>
import ticketItem from './TicketItem'
export default {
  name: 'TicketItem',
  data () {
    return {
      showTicket: false
    }
  },
  components: {
    ticketItem
  },
  methods: {
    toggleTicketItem () {
      this.showTicket = !this.showTicket
    }
  }
}
</script>

<style lang="stylus" scoped>
::before
  z-index 3
.ticket-list
  overflow hidden
  .ticket-list-info
    position relative
    padding .24rem .2rem
    background #fff
    .ticket-name
      margin-right 1.8rem
      color #333
      font-size .3rem
      line-height .48rem
    .ticket-price
      overflow hidden
      position absolute
      top 50%
      margin-top -.28rem
      right .26rem
      height .4rem
      line-height .4rem
      font-size .24rem
      color #ff9800
      .price-num
        font-size .4rem
        margin-left .04rem
      .price-numword
        display inline-block
        font-size .24rem
        color #9e9e9e
        transform scale(.8)
      .icon
        color #9e9e9e
        font-size .3rem
  .ticket-item
    padding .2rem
    background #f5f5f5
    >>> .ticket-title
      font-size .28rem
      line-height .4rem
</style>
