<template>
    <div class="play">
        <div class="left">
            <div class="play-img">
                <img src="http://p1.music.126.net/rxyLRMZdqzHdxyP5cl8qQA==/43980465112095.jpg?param=130y130" class="play-item-img">
            </div>
            <div class="play-info">
                <div class="info-title">遥远的她</div>
                <div class="info-desc">横滑可以切换上下首哦</div>
            </div>
        </div>
        <div class="right">
            <div class="right-border border">
                <span class="iconfont">&#xe769;</span>
            </div>
            <span class="iconfont list-play">&#xe769;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomePlay'
}
</script>

<style lang="stylus" scoped>
  .play
    width: 100%
    height: 0
    padding-bottom: 14%
    background: #fff
    margin-top: .2rem
    border-top: 0.01rem solid #ccc
    .left
      float: left
      margin-left: .2rem
      margin-top: .1rem
      .play-img
        width: .98rem
        height: .98rem
        background: red
        border-radius: 50%
        overflow: hidden
        float: left
        .play-item-img
          width: 100%
      .play-info
        float: left
        margin-left: .1rem
        .info-title
          line-height: .6rem
          font-size: .28rem
        .info-desc
          font-size: .24rem
    .right
      float: right
      margin-right: .2rem
      .right-border
        margin-top: .2rem
        width: .5rem
        height: .5rem
        line-height: .5rem
        text-align: center
        border-radius: 50%
        float: left
        border: 0.01rem solid black
        margin-right: .4rem
      .list-play
        margin-top: .3rem
        display: block
        float: left
</style>
