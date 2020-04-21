<template>
    <div class="icons">
        <div class="icons-item">
            <div class="icons-item-img">
                <span class="iconfont icont-img one">&#xe601;</span>
            </div>
            <div class="icons-item-info">
                每日推荐
            </div>
        </div>
        <div class="icons-item">
            <div class="icons-item-img">
                <span class="iconfont icont-img tow">&#xe602;</span>
            </div>
            <div class="icons-item-info">
                歌单
            </div>
        </div>
        <div class="icons-item">
            <div class="icons-item-img">
                <span class="iconfont icont-img three">&#xe604;</span>
            </div>
            <div class="icons-item-info">
                排行榜
            </div>
        </div>
        <div class="icons-item">
            <div class="icons-item-img">
                <span class="iconfont icont-img four">&#xe65e;</span>
            </div>
            <div class="icons-item-info">
                电台
            </div>
        </div>
        <div class="icons-item">
            <div class="icons-item-img">
                <span class="iconfont icont-img five">&#xe62f;</span>
            </div>
            <div class="icons-item-info">
                私人FM
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  .icons
    height: 0
    padding-bottom: 20%
    overflow: hidden
    .icons-item
      width: 20%
      overflow: hidden
      float: left
      .icons-item-img
        width: 60%
        height: 0
        padding-bottom: 60%
        background: red
        border-radius: 50%
        margin: 0 auto
        position: relative
        .icont-img
          color: #fff
          position: absolute
        .one
          font-size: 1rem
        .tow
          font-size: .58rem
          top: .2rem
          left: .2rem
        .three
          font-size: .58rem
          top: .2rem
          left: .2rem
        .four
          font-size: .58rem
          top: .21rem
          left: .21rem
        .five
          font-size: .58rem
          top: .18rem
          left: .18rem
      .icons-item-info
        width: 100%
        height: 0
        padding-bottom: 40%
        overflow: hidden
        text-align: center
        line-height: .6rem
</style>
