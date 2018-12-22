<template>
  <div class="comment-item border-top">
    <div class="comment-stardate">
      <star class="comment-star" :size="24" :score="5"></star>
      <span class="comment-date">v**z&nbsp;&nbsp;&nbsp;2018-09-05</span>
    </div>
    <!--使用三元运算判断-->
    <p class="comment-content" :style="auto ? fold: unfold">参观故宫是来京必须要安排的行程，紫禁城的宏伟和惊艳超乎你想象，假装自己穿越时空，你走在乾隆皇帝走过的石板砖上，体验当年盛世的文化底蕴和奢华的生活～ 攻略1 提前网上购买门票，凭身份证直接进 攻略2 租讲解器，每个讲解器都是感应的，每个只讲解一遍，只有一个耳机，别想着两人共用的好事儿，哈哈哈 攻略3 周一闭馆，周末人居多，尽量安排工作日，若所有宫殿都想参观，就提早进去，不过我个人觉得没必要，参观代表性的中轴和个别妃子和慈禧的宫殿即可，建议预留至少大半天时间在里头 再来北京，还愿意去故宫~~～</p>
    <div class="comment-foldbtn" @click="toggleFold">
      <svg class="icon" aria-hidden="true">
        <use xlink:href="#icon-jiantou-xia" v-show="!auto"></use>
        <use xlink:href="#icon-jiantou-shang" v-show="auto"></use>
      </svg>
    </div>
    <ul class="comment-imgs" @click="toggleGallery">
      <li class="comment-imgouter" v-for="(item, index) of imgs" :key="index">
        <div class="comment-imginner">
          <img class="comment-img" :src="item">
        </div>
      </li>
    </ul>
    <fade-animation>
      <common-gallery :imgs="imgs"
      v-show="showGallery" @closeGallery="toggleGallery">
      </common-gallery>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
import star from 'common/star/star'
import FadeAnimation from 'common/Fade'
export default {
  name: 'CommentItem',
  data () {
    return {
      auto: false,
      fold: {
        height: 'auto',
        overflow: 'auto'
      },
      unfold: {
        height: '105px',
        overflow: 'hidden'
      },
      showGallery: false,
      imgs: [
        'https://imgs.qunarzz.com/piao/fusion/1811/d6/fd836aeebb7d1b02.jpg_228x168_4da11645.jpg',
        'https://imgs.qunarzz.com/piao/fusion/1811/11/9315fd108bdb0c02.jpg_228x168_a1e9ad7f.jpg',
        'https://imgs.qunarzz.com/piao/fusion/1811/a2/72f1b6ea30212d02.jpg_228x168_cd9788d3.jpg',
        'https://imgs.qunarzz.com/piao/fusion/1811/dd/f64ae8772d0dda02.jpg_228x168_8fe347a5.jpg'
      ]
    }
  },
  methods: {
    toggleFold (e) {
      this.auto = !this.auto
    },
    toggleGallery () {
      this.showGallery = !this.showGallery
    }
  },
  components: {
    star,
    CommonGallery,
    FadeAnimation
  }
}
</script>

<style lang="stylus" scoped>
.comment-item
  padding .1rem .2rem .3rem .2rem
  .comment-stardate
    margin-top .1rem
    height .6rem
    .comment-star
      position relative
      display inline-block
      // width 1.5rem
      top .14rem
      >>> .star-item
        width 12px
        height 12px
        background-size 12px 12px
    .comment-date
      position relative
      float right
      top .16rem
      margin-left .2rem
      height .28rem
      line-height .28rem
      font-size .24rem
  .comment-content
    overflow hidden
    height 105px
    line-height .42rem
    font-size .26rem
    color #616161
  .comment-foldbtn
    height .48rem
    line-height .48rem
    text-align center
    .icon
      font-size .35rem
      color #9e9e9e
  .comment-imgs
    position relative
    display flex
    flex-wrap wrap
    margin .2rem 0 .1rem 0
    overflow hidden
    .comment-imgouter
      flex 0 0 33.3333%
      .comment-imginner
        margin 0 .07rem
        .comment-img
          width 100%
</style>
