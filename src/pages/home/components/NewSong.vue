<template>
    <div class="song">
        <div class="title">
            <div class="title-info">新歌 | 新碟</div>
            <div class="title-btn border">
                更多新歌
            </div>
        </div>
        <ul class="item">
            <li class="item-list">
              <div class="item-wrapper">
                <img class="item-img" src="http://p3.music.126.net/VoOnN18xSPNWl-a-GEoJpA==/109951164903592379.jpg?param=130y130" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">煎熬 - 尹毓恪</div>
                  <div class="item-info-desc">
                    <span class="item-desc-left">独家</span>
                    <span class="item-desc-right">陷的太深的海底 只能依靠自己</span>
                  </div>
                </div>
                <div class="item-player border">
                  <span class="iconfont">&#xe62b;</span>
                </div>
              </div>
            </li>
            <li class="item-list">
              <div class="item-wrapper">
                <img class="item-img" src="http://p3.music.126.net/70aqeNGo-m7rFRzQ9NhFaQ==/109951164900505375.jpg?param=130y130" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">Look For The Good - Jason Mraz</div>
                  <div class="item-info-desc">
                    <span class="item-desc-left">独家</span>
                    <span class="item-desc-right">有让人变得快乐的魔力呀</span>
                  </div>
                </div>
                <div class="item-player border">
                  <span class="iconfont">&#xe62b;</span>
                </div>
              </div>
            </li>
            <li class="item-list">
              <div class="item-wrapper">
                <img class="item-img" src="http://p4.music.126.net/sUV5ofnck1GwfdrtHAS--g==/109951164864019028.jpg?param=130y130" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">PEOPLE - Code Kunst</div>
                  <div class="item-info-desc">
                    <span class="item-desc-left">独家</span>
                    <span class="item-desc-right">Code Kunst</span>
                  </div>
                </div>
                <div class="item-player border">
                  <span class="iconfont">&#xe62b;</span>
                </div>
              </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeNewSong'
}
</script>

<style lang="stylus" sceped>
  .song >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .song
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 70%
    background: #fff
    margin-top: .4rem
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
        .player
          color: black
    .item
      width: 100%
      height: 5.15rem
      margin-top: 0.04rem
      .item-list
        width: 100%
        height: 1.3rem
        background: #fff
        margin-bottom: .4rem
        position: relative
        .item-wrapper
          width: 1.3rem
          height: 1.3rem
          overflow: hidden
          margin-left: .2rem
          border-radius: .2rem
          float: left
          .item-img
            width: 100%
            border-radius: .2rem
      .item-info
          float: left
          margin-left: .2rem
          height: 1.3rem
          display: flex
          .left
            .item-info-title
              font-weight: 600
              height: .5rem
              line-height: .5rem
            .item-info-desc
              line-height: .8rem
              .item-desc-left
                color: red
                font-size: .2rem
                border: 0.01rem solid red
                padding: 0.01rem
              .item-desc-right
                color: rgba(0,0,0,0.5)
                font-size: .30rem
          .item-player
            width: .5rem
            height: .5rem
            position: absolute
            border-radius: 50%
            top: .4rem
            right: .6rem
            text-align: center
            line-height: .5rem
            color: red
</style>
