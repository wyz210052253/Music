<template>
    <div>
        <home-header></home-header>
        <home-banner></home-banner>
        <home-icons></home-icons>
        <home-recommend></home-recommend>
        <home-re-style></home-re-style>
        <home-scene></home-scene>
        <home-new-song></home-new-song>
        <home-player></home-player>
        <home-ranking></home-ranking>
        <home-broadcast></home-broadcast>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeBanner from './components/Banner'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeReStyle from './components/ReStyle'
import HomeScene from './components/SceneRecommend'
import HomeNewSong from './components/NewSong'
import HomePlayer from './components/Player'
import HomeRanking from './components/Ranking'
import HomeBroadcast from './components/Broadcast'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeBanner,
    HomeIcons,
    HomeRecommend,
    HomeReStyle,
    HomeScene,
    HomeNewSong,
    HomePlayer,
    HomeRanking,
    HomeBroadcast
  }
}
</script>

<style lang='stylus' scoped>

</style>
