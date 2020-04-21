<template>
    <div class="recommend">
        <div class="title">
            <div class="title-info">推荐歌单</div>
            <div class="title-btn border">
                查看更多
            </div>
        </div>
        <div class="wrapper">
            <div class="content" v-for="item of list" :key='item.id'>
                <div class="content-img">
                    <img class="item-img" :src="item.url">
                    <div class="item-img-play">
                        <span class="iconfont">&#xe769;</span>{{item.play}}
                    </div>
                </div>
                <p class="content-desc">
                    {{item.desc}}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      list: [{
        id: '0001',
        url: 'http://p1.music.126.net/8x-pNz7EmZ9Abgxqg7GkyQ==/109951164922813123.jpg?param=140y140',
        desc: '[华语速爆新歌] 最新华语音乐推荐',
        play: '7.9亿'
      },
      {
        id: '0002',
        url: 'http://p2.music.126.net/fJLmA2YMx-3rpbFeyiTp9Q==/109951164857220634.jpg?imageView=1&type=webp&thumbnail=369x0',
        desc: '艺术流行 ‖ 领悟音乐的折衷主义',
        play: '5399万'
      },
      {
        id: '0003',
        url: 'http://p2.music.126.net/9raCbkcdTiXiOcToKh1XRQ==/109951164515936501.jpg?imageView=1&type=webp&thumbnail=369x0',
        desc: '循环播放的神仙歌单',
        play: '1.5亿'
      },
      {
        id: '0004',
        url: 'http://p2.music.126.net/Le3bvcB8dBLqpsTpnJHwyg==/109951164569849121.jpg?imageView=1&type=webp&thumbnail=369x0',
        desc: '音乐烘焙店♬售卖人间烟火 烘焙星辰大海',
        play: '1.3亿'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .recommend >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .recommend
    margin-top: .3rem
    width: 100%
    height: 0
    padding-bottom: 46%
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
      height: 3.21rem
      width: 100%
      .content
        width: 25%
        height: 3.11rem
        overflow: hidden
        margin-top: .1rem
        float: left
        .content-img
          width: 90%
          height: 2.2rem
          margin: .1rem auto
          border-radius: .2rem
          position: relative
          .item-img
            width: 100%
            border-radius: .2rem
          .item-img-play
            position: absolute
            top: .08rem
            left: .7rem
            color: #fff
            font-size: .2rem
        .content-desc
          width: 100%
          padding: 0 .1rem
          word-wrap: wrap
          box-sizing: border-box
          line-height: .36rem
          text-align: center
</style>
