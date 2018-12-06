<template>
  <div id="main-page">
    <city-header></city-header>
    <city-search :cities="cities"></city-search>
    <city-list
       :cities="cities"
       :hotCities="hotCities"
       :letter="letter">
    </city-list>
    <city-alphabet
       :cities="cities"
       @change="handleLetterChange">
    </city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/CityHeader'
import CitySearch from './components/CitySearch'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
import axios from 'axios'
// import BScroll from 'better-scroll'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      cities: {},
      hotCities: [],
      letter: ''
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.getCityInfoSuc)
    },
    getCityInfoSuc (res) {
      res = res.data
      if (res.ret && res.data) {
        this.cities = res.data.cities
        this.hotCities = res.data.hotCities
      }
    },
    handleLetterChange (letter) {
      this.letter = letter
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
@import '~styles/varibles.styl'
#main-page
  background #f5f5f5
</style>
