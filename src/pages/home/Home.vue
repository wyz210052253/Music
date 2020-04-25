<template>
    <div>
        <home-header class="header"></home-header>
        <home-banner :list="bannerList"></home-banner>
        <home-icons></home-icons>
        <home-recommend :list="recommendList"></home-recommend>
        <home-re-style :list="restyleList"></home-re-style>
        <home-scene :list="sceneList"></home-scene>
        <home-new-song :list="songList"></home-new-song>
        <home-player :list="playerList"></home-player>
        <home-ranking :list="rankingList"></home-ranking>
        <home-broadcast :list="broadcastList"></home-broadcast>
        <router-link to="/player">
          <home-play class="footer"></home-play>
        </router-link>
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
import HomePlay from './components/Play'
import axios from 'axios'
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
    HomeBroadcast,
    HomePlay
  },
  data () {
    return {
      bannerList: [],
      recommendList: [],
      restyleList: [],
      sceneList: [],
      songList: [],
      playerList: [],
      rankingList: [],
      broadcastList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/home.json').then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.bannerList = data.BannerList
        this.recommendList = data.RecommendList
        this.restyleList = data.reStyle
        this.sceneList = data.sceneList
        this.songList = data.songList
        this.playerList = data.playerList
        this.rankingList = data.rankingList
        this.broadcastList = data.broadcastList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style lang='stylus' scoped>
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
    color: #000
</style>
