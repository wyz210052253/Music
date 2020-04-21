<template>
    <div class="restyle">
        <div class="title">
            <div class="title-info">风格推荐</div>
            <div class="title-btn border">
                <span class="iconfont player">&#xe62b;</span>
                播放全部
            </div>
        </div>
        <ul class="item">
            <li class="item-list">
              <div class="item-wrapper">
                <img class="item-img" src="http://p2.music.126.net/9raCbkcdTiXiOcToKh1XRQ==/109951164515936501.jpg?param=140y140" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">Rags To Rings - Danny Mc Carthy</div>
                  <span class="item-info-desc">超23%人收藏</span>
                </div>
                <div class="item-player border">
                  <span class="iconfont">&#xe62b;</span>
                </div>
              </div>
            </li>
            <li class="item-list">
              <div class="item-wrapper">
                <img class="item-img" src="http://p3.music.126.net/6nuFSMK3UMG5nLsreYX1Vg==/109951164862495860.jpg?param=100y100" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">Uptown Funk -Mark Ronson</div>
                  <span class="item-info-desc-two">守望先锋好莱坞推车必备</span>
                </div>
                <div class="item-player border">
                  <span class="iconfont">&#xe62b;</span>
                </div>
              </div>
            </li>
            <li class="item-list">
              <div class="item-wrapper">
                <img class="item-img" src="http://p4.music.126.net/bZxfyuY58soD71VGxv6BDQ==/109951164814715844.jpg?param=100y100" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">Heist - Noisestorm</div>
                  <span class="item-info-desc-two">绝地求生精彩集锦必备BGM</span>
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
  name: 'HomeReStyle'
}
</script>

<style lang="stylus" scoped>
  .restyle >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .restyle >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .restyle
    margin-top: .5rem
    width: 100%
    height: 0
    padding-bottom: 70%
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
              color: red
              background: rgba(198,47,47,0.3)
              padding: 0.1rem
              border-radius: .1rem
            .item-info-desc-two
              line-height: .8rem
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
