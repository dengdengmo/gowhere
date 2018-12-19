<template>
  <div class="ticket-list border-bottom">
    <div class="ticket-list-info">
      <h5 class="ticket-name" @click="toggleTicketItem">上午场</h5>
      <div class="ticket-price">
        ￥<em class="price-num">40</em><span class="price-numword">起</span>
      </div>
      <span class="ticketList-icon"></span>
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
      right .46rem
      height .4rem
      line-height .4rem
      font-size .24rem
      color #ff9800
      .price-num
        font-size .4rem
        margin-left .04rem
      .price-numword
        color #9e9e9e
  .ticket-item
    padding .2rem
    background #f5f5f5
    >>> .ticket-title
      font-size .28rem
      line-height .4rem
</style>
