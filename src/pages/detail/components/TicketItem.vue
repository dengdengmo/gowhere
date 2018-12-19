<template>
  <div class="ticket-item border-top">
      <div class="ticket-main">
        <div>
          <h6 class="ticket-title">八达岭长城门票+索道/地面缆车往返成人票（淡季）</h6>
          <ul class="ticket-light">
            <span class="ticekt-desctag">
              <img class="ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png">
              可订明日
            </span>
          </ul>
          <ul class="ticket-labelcon">
            <span class="ticket-label">
              <img class="ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png">自营
            </span>
            <span class="ticket-label">随时退</span>
          </ul>
        </div>
      </div>
      <div class="ticket-side">
        <strong class="price">
          ￥<em class="price-num">175</em>
        </strong>
        <em class="ticket-btn">预定</em>
      </div>
  </div>
</template>

<script>
export default {
  name: 'TicketItem'
}
</script>

<style lang="stylus" scoped>
.ticket-item
  box-sizing border-box
  padding .2rem .2rem .24rem 0
  display flex
  width 100%
  .ticket-main
    flex 2.92
    .ticket-title
      margin-right .1rem
      line-height .52rem
      padding 0
      font-size .3rem
    .ticket-light
      overflow hidden
      .ticekt-desctag
        display inline-block
        height .32rem
        line-height .32rem
        font-size .24rem
        color #616161
        white-space nowrap
        .ticket-tagicon
          display inline-block
          width .2rem
          max-height .32rem
          margin-right .04rem
          vertical-align 0
    .ticket-labelcon
      font-size 0
      .ticket-label
        display inline-block
        margin-top .08rem
        padding 0 .04rem
        height .32rem
        line-height .32rem
        color #00afc7
        font-size .2rem
        white-space nowrap
        .ticket-tagicon
          display inline-block
          width .2rem
          max-height .32rem
          margin-right .04rem
          vertical-align 0
        &:not(:last-child)
          margin-right .1rem
  .ticket-side
    flex 1
    display flex
    flex-direction column
    justify-content center
    .price
      display block
      overflow hidden
      color #ff9800
      height .4rem
      font-size .24rem
      text-align center
      .price-num
        margin-left .04rem
        font-size .4rem
        height .4rem
    .ticket-btn
      display block
      height .6rem
      color #ffffff
      line-height .6rem
      border-radius .08rem
      text-align center
      background-image linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%)
</style>
