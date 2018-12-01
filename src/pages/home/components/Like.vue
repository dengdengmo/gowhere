<template>
  <div class="group">
    <div class="group-title">
      <img  class="title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="猜你喜欢">
      <span class="title">猜你喜欢</span>
    </div>
    <ul class="like-list">
      <li class="like-item border-bottom">
        <div class="like-imgcon">
          <img src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg" alt="" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">故宫</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="5"></star>
            <span class="comment-num">334545条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">20</em>
            </span>
            起
            <span class="like-addres">东城区</span>
          </div>
        </div>
      </li>
      <li class="like-item border-bottom">
        <div class="like-imgcon">
          <img src="http://img1.qunarzz.com/sight/p0/1711/53/53f7752ece875d00a3.img.jpg_200x200_5c006913.jpg" alt="" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">龙脉温泉</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="4.8"></star>
            <span class="comment-num">486条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">156</em>
            </span>
            起
            <span class="like-addres">昌平区</span>
          </div>
        </div>
      </li>
      <li class="like-item border-bottom">
        <div class="like-imgcon">
          <img src="http://img1.qunarzz.com/sight/p0/1608/5c/5c30160572493ba9a3.water.jpg_200x200_8ded77a0.jpg" alt="" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">北京乐多港奇幻乐园</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="4.2"></star>
            <span class="comment-num">857条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">20</em>
            </span>
            起
            <span class="like-addres">东城区</span>
          </div>
        </div>
      </li>
      <li class="like-item border-bottom">
        <div class="like-imgcon">
          <img src="http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg" alt="" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">北京野生动物园</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="3.6"></star>
            <span class="comment-num">17775条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">71</em>
            </span>
            起
            <span class="like-addres">大兴区</span>
          </div>
        </div>
      </li>
      <li class="like-item border-bottom">
        <div class="like-imgcon">
          <img src="http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg" alt="" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">八达岭长城</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="4.8"></star>
            <span class="comment-num">42939条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">157.5</em>
            </span>
            起
            <span class="like-addres">大兴区</span>
          </div>
        </div>
      </li>
      <li class="like-item border-bottom">
        <div class="like-imgcon">
          <img src="http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg" alt="" class="like-img">
        </div>
        <div class="like-info">
          <div class="like-title">北京欢乐谷</div>
          <div class="like-comment">
            <star class="star-level" :size="24" :score="2.3"></star>
            <span class="comment-num">65829条评论</span>
          </div>
          <div class="like-price">
            <span class="price">
              ￥<em class="price-num">157.5</em>
            </span>
            起
            <span class="like-addres">大兴区</span>
          </div>
        </div>
      </li>
      <a href="" class="like-more border-top">查看所有产品</a>
    </ul>
  </div>
</template>

<script>
import star from '../components/star/star'
export default {
  name: 'HomeLike',
  components: {
    star
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.group
  margin-top .2rem
  background #fff
  .group-title
    position relative
    padding .24rem 0 .26rem
    .title-img
      title-img()
    .title
      title()
  .like-list
    margin-left .24rem
    .like-item
      overflow hidden
      padding .2rem 0
      .like-imgcon
        float left
        overflow hidden
        width 2rem
        height 2rem
        .like-img
          width 100%
      .like-info
        overflow hidden
        padding-left .22rem
        .like-title
          margin-top .26rem
          color #212121
          font-size .32rem
          height .44rem
          line-height .44rem
        .like-comment
          margin-top .14rem
          height .34rem
          font-size 0
          .star-level
            display inline-block
            position relative
            width 1.7rem
            height .28rem
            line-height .28rem
            transform scale(1.16)
            transform-origin left
          .comment-num
            color #616161
            font-size .24rem
            line-height .34rem
        .like-price
          margin-top .22rem
          position relative
          color #616161
          font-size .24rem
          line-height .4rem
          .price
            color $priceColor
            .price-num
              font-size .4rem
          .like-addres
            position absolute
            right .24rem
    .like-more
      display block
      padding .2rem 0
      color #00afc7
      font-size .28rem
      line-height .4rem
      text-align center
</style>
