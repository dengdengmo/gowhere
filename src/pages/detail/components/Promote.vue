<template>
  <div class="promote">
    <h3 class="promote-title border-bottom">去哪儿推荐</h3>
    <ticket-item></ticket-item>
    <ticket-item></ticket-item>
    <ticket-item></ticket-item>
  </div>
</template>

<script>
import ticketItem from './TicketItem'
export default {
  name: 'DetailPromote',
  components: {
    ticketItem
  }
}
</script>

<style lang="stylus" scoped>
.promote
  position relative
  margin-bottom .2rem
  padding-left .2rem
  background #fff
  .promote-title
    overflow hidden
    position relative
    padding 0 .2rem
    margin-bottom -.02rem
    font-size .32rem
    height .88rem
    line-height .88rem
    color #333
    text-indent .36rem
    background url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAMAAABg3Am1AAAAflBMVEUAAAD/bm7/b2//b2//eXn/b2//b2//bm7/b2//b2//bm7/b2//b2//b2//bm7/b2//b2//cXH/eHj/qqr/bm7/////cXH/iIj/oqL//f3/mJj/fHz/9/f/8PD/4eH/ycn/6+v/1dX/0ND/t7f/ra3/kpL/jo7/c3P/5ub/vr7o37bEAAAAFHRSTlMA9uZeCfny7NvLt6+PfGZONxsRA/pz1k8AAAFrSURBVEjHpZbZdoMwDERtMEvYE8YJZN/b/v8PNvicJsiYqJzcB548WGNZksUAVWZJHAVBFCdZqQTDwk8lesjUX4hxVB5iQJiPbVMXHpx4RS0czGcYZTYXAyoPb/AqYeFLvEX61nqwEEUlwSKrnl9X/JtmZfl4Oq9d53Pfan2yzurvdAs42OsHaxAKYVDOA207wcEKShlBDhfaIUBu7lsIl2UjuIASLkZTsDaCxpWMFC7ORrCBRfqw7MxZY9Z/w0YqUWLI8tLqJ+25n8BSZP3Am+aG2/Vw1IQ9XmQiwZNV9z+0mkKtJCKmAg094IgXsYg4Ab0gkQh4wRUvgv8I1kTAh7QHCYk3fQIxnbCCHXokImMFPyCJKznB9gvkaijJ7XCnl0+kU3ZISQFttp3DnWW5oQVES3S57D4Eq0RJE+DJSZvh8RRpZDwFaZU8s5o0YxZvPrXdTx0on40sfih+Nnb5wT7x6fDR42Ty8+cXnHyOvDgQEbUAAAAASUVORK5CYII=')
    background-size .36rem .36rem
    background-repeat no-repeat
    background-position 0 center
</style>
