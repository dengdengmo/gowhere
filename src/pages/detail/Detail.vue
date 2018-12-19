<template>
  <div class="main-page">
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-baseinfo></detail-baseinfo>
    <div class="ticket-container">
      <detail-promote></detail-promote>
      <ticket-tab></ticket-tab>
      <ticket-group id="anchor_1" data-anchor="1"></ticket-group>
      <ticket-group></ticket-group>
      <ticket-group></ticket-group>
      <ticket-group id="anchor_2" data-anchor="2"></ticket-group>
      <ticket-group></ticket-group>
      <ticket-group></ticket-group>
      <ticket-group id="anchor_3" data-anchor="3"></ticket-group>
      <ticket-group></ticket-group>
      <ticket-group></ticket-group>
      <ticket-group id="anchor_4" data-anchor="4"></ticket-group>
    </div>
    <div class="content"></div>
  </div>
</template>

<script>
import detailBanner from './components/Banner'
import detailHeader from './components/Header'
import detailBaseinfo from './components/Baseinfo'
import detailPromote from './components/Promote'
import ticketGroup from './components/TicketGroup'
import ticketTab from './components/TicketTab'
export default {
  name: 'Detail',
  components: {
    detailBanner,
    detailHeader,
    detailBaseinfo,
    detailPromote,
    ticketGroup,
    ticketTab
  },
  methods: {
  }
}
</script>

<style lang="stylus" scoped>
.main-page
  background #f5f5f5
  .content
    height 50rem
</style>
