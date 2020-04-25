<template>
    <div>
      <search-header class="header"></search-header>
      <search-banner></search-banner>
      <search-history></search-history>
      <search-hot></search-hot>
      <home-play class="footer"></home-play>
    </div>
</template>

<script>
import SearchHeader from './components/Header'
import SearchBanner from './components/Banner'
import SearchHistory from './components/History'
import SearchHot from './components/HotSearch'
import HomePlay from './components/Play'
export default {
  name: 'Search',
  components: {
    SearchHeader,
    SearchBanner,
    SearchHistory,
    SearchHot,
    HomePlay
  }
}
</script>

<style lang="stylus" scoped>
  .header
    position: fixed
    top: 0
    z-index: 10
    width: 100%
    background: #fff
  .footer
    position: fixed
    bottom: 0
    width: 100%
    background: #fff
    z-index: 10
</style>
