<template>
  <div id="qunarFooter">
    <div class="main_nav-wrapper">
      <ul class="main_nav" :style="show ? more : ''" id="qunarFooterUL">
        <li class="flight">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">机票</span>
          </a>
        </li>
        <li class="hotel">
          <a href="#">
          <div class="footer-icon"></div>
          <span class="title">酒店</span>
          </a>
        </li>
        <li class="gongyu">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">公寓</span>
          </a>
        </li>
        <li class="tuan">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">团购</span>
          </a>
        </li>
        <li class="train">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">火车票</span>
          </a>
        </li>
        <li class="jingdian">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">景点</span>
          </a>
        </li>
        <li class="zuche">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">接送机</span>
          </a>
        </li>
        <li class="dujia">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">度假</span>
          </a>
        </li>
        <li class="gonglue">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">攻略</span>
          </a>
        </li>
        <li class="lvtu">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">旅途</span>
          </a>
        </li>
        <li class="cheche">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">车车</span>
          </a>
        </li>
        <li class="dangdiren">
          <a href="#">
            <div class="footer-icon"></div>
            <span class="title">当地人</span>
          </a>
        </li>
        <li class="tag" :style="show ? top : ''" @click="showMore">
          <div class="more-wrapper">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-zhankai" v-show="!show"></use>
              <use xlink:href="#icon-shouqi" v-show="show"></use>
            </svg>
            <span class="txt">更多</span>
          </div>
        </li>
      </ul>
    </div>
    <ul class="footer_nav border-bottom">
      <li><a href="">登录</a></li>
      <li><a href="">我的订单</a></li>
      <li><a href="">最近浏览</a></li>
      <li><a href="">关于我们</a></li>
    </ul>
    <ul class="mobile_PC">
      <li class="active">
        <a href="#">触屏版</a>
      </li>
      <li>
        <a href="#">电脑版</a>
      </li>
    </ul>
    <div class="copyright">
      <span>Qunar 京ICP备05021087</span>
      <a href="#">意见反馈</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'qunarFooter',
  data () {
    return {
      show: false,
      more: {
        height: '93px',
        padding: '10px 10px 25px 10px'
      },
      top: {
        top: '97px'
      }
    }
  },
  methods: {
    showMore () {
      this.show = !this.show
    }
  }
}
</script>

<style lang="stylus" scoped>
#qunarFooter
  background #f3f3f3
  .main_nav
    position relative
    display flex
    flex-wrap wrap
    width 300px
    height 25px
    margin 0 auto
    padding 10px 10px 0 10px
    overflow hidden
    li
      flex 65px
      margin 0
      padding-left 10px
      height 31px
      width 65px
      position relative
      overflow auto
      .footer-icon
        float left
        width 22px
        height 22px
        background url(//source.qunarzz.com/site/images/wap/touch/images/v2/images2x/nav_7.png) 0 0 no-repeat
        background-size 175px 50px
      .title
        float left
        display inline-block
        color #9e9e9e
        margin 3px 0 0 5px
        border-bottom 1px solid #acacac
        font-size 12px
    .tag
      position absolute
      top 8px
      right 6px
      width 70px
      font-size 0
      color #9e9e9e
      background #f3f3f3
      .more-wrapper
        padding-left 17px
        // margin-top 2px
        border-left 1px solid #9e9e9e
        .txt
          font-size 14px
        .icon
          font-size 18px
          vertical-align -3px
    .flight
      .footer-icon
        background-position 0 0
    .hotel
      .footer-icon
        background-position -25px 0
    .gongyu
      .footer-icon
        background-position -150px 0
    .tuan
      .footer-icon
        background-position -50px 0
    .train
      .footer-icon
        background-position -50px -25px
    .jingdian
      .footer-icon
        background-position -75px 0
    .zuche
      .footer-icon
        background-position -100px 0
    .dujia
      .footer-icon
        background-position 0 -25px
    .gonglue
      .footer-icon
        background-position -75px -25px
    .lvtu
      .footer-icon
        background-position -100px -25px
    .cheche
      .footer-icon
        background-position -125px 0
    .dangdiren
      .footer-icon
        background-position -125px -25px
  .footer_nav
    display flex
    width 100%
    height 37px
    line-height 37px
    li
      flex 1
      text-align center
  .mobile_PC
    padding-top 10px
    text-align center
    li
      display inline-block
      margin 0 15px
    .active a
      color #9e9e9e
  .copyright
    padding 10px
    font-size 14px
    color #9e9e9e
    text-align center
    a
      color #9e9e9e
</style>
