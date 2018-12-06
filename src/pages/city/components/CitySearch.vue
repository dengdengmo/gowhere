<template>
  <div>
    <div class="search">
      <input class="search-input" v-model="keyword" ref="input" type="text" placeholder="输入城市名或拼音"/>
    </div>
    <div class="search-content" v-show="keyword">
      <ul class="search-list">
        <li class="search-item border-bottom" v-for="item of list" :key="item.id">
          {{item.name}}
        </li>
        <li class="search-item border-bottom" v-show="!this.hasData">
          没有匹配城市
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  computed: {
    hasData () {
      return this.list.length
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((item) => {
            if (item.spell.indexOf(this.keyword) > -1 ||
                item.name.indexOf(this.keyword) > -1) {
              result.push(item)
            }
          })
        }
        this.list = result
      }, 200)
    }
  },
  mounted () {
    this.$refs.input.onfocus = () => {
      this.$refs.input.placeholder = ''
    }
    this.$refs.input.onblur = () => {
      this.$refs.input.placeholder = '输入城市名或拼音'
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
@import '~styles/varibles.styl'
.search
  height .72rem
  padding 0 .1rem
  background #00bcd4
  .search-input
    box-sizing border-box
    width 100%
    height .62rem
    padding 0 .1rem
    line-height .62rem
    border-radius .06rem
    text-align center
    color #666
    &::-webkit-input-placeholder
      color #ccc
      font-size .26rem
.search-content
  position absolute
  top 1.58rem
  right 0
  left 0
  bottom 0
  background #eee
  z-index 1
  .search-item
    line-height .62rem
    padding-left .2rem
    color #666
    background #fff
</style>
