<template>
    <div class="broadcat">
        <div class="title">
            <div class="title-info">电台推荐</div>
            <div class="title-btn border">
                查看更多
            </div>
        </div>
        <div class="wrapper">
            <div class="content" v-for="item of list" :key="item.id">
                <div class="content-img">
                    <img class="item-img" :src="item.imgUrl">
                    <div class="item-img-play">
                        <span class="iconfont player">&#xe62b;</span>
                    </div>
                </div>
                <div class="content-info">
                    <div class="info-title">{{item.title}}</div>
                    <div class="info-desc">{{item.desc}}</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeBroadcast',
  data () {
    return {
      list: [{
        id: '0001',
        imgUrl: 'http://p2.music.126.net/Y7cveTgV3qbYTwqJ2FNnBw==/109951164526625758.jpg?param=140y140',
        title: '孤独解药',
        desc: '一首歌，一晚好梦'
      }, {
        id: '0002',
        imgUrl: 'http://p1.music.126.net/ipDaITvu_vVvHJqxaujLUQ==/109951164441184008.jpg?param=140y140',
        title: '心是孤独的猎手',
        desc: '人越是明白，就越是孤独'
      }, {
        id: '0003',
        imgUrl: 'http://p1.music.126.net/nBZdICm9wJOo4tqy8jIfLA==/109951164002262205.jpg?param=140y140',
        title: '最怕碌碌无为',
        desc: '陪着你,一起仗剑走天涯'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .broadcat >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .broadcat
    margin-top: .3rem
    width: 100%
    height: 0
    padding-bottom: 49%
    background: #fff
    .title
      width: 100%
      height: .6rem
      line-height: .6rem
      overflow: hidden
      .title-info
        font-size: .4rem
        font-weight: bold
        float: left
        margin-left: .2rem
      .title-btn
        float: right
        margin-right: .2rem
        width: 1.8rem
        text-align: center
        height: .5rem
        line-height: .5rem
        margin-top: .05rem
    .wrapper
      height: 3.46rem
      width: 96%
      margin: 0 auto
      overflow: hidden
      .content
        width: 28%
        height: 3.11rem
        margin-top: .1rem
        margin-right: .3rem
        margin-left: .1rem
        float: left
        .content-img
          width: 100%
          border-radius: .2rem
          position: relative
          .item-img
            width: 100%
            border-radius: .2rem
          .item-img-play
            position: absolute
            right: .2rem
            bottom: .2rem
            width: .5rem
            height: .5rem
            line-height: .5rem
            text-align: center
            border-radius: 50%
            background: rgba(255,255,255,0.5)
            .player
              color: red
        .content-info
          width: 100%
          .info-title
            text-align: left
            line-height: .5rem
            font-size: .28rem
          .info-desc
            text-align: left
            font-size: .24rem
</style>
