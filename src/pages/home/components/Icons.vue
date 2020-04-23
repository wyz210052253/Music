<template>
    <div class="icons" ref="wrapper">
        <div class="icons-list" ref="personTab">
          <div class="icons-item" ref="item">
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
          <div class="icons-item">
              <div class="icons-item-img">
                  <span class="iconfont icont-img six">&#xe630;</span>
              </div>
              <div class="icons-item-info">
                  歌手专区
              </div>
          </div>
        </div>
    </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'HomeIcons',
  methods: {
    personScroll () {
      let width = 6 * this.$refs.item.offsetWidth
      this.$refs.personTab.style.width = width + 'px'
      this.$nextTick(() => {
        if (!this.scroll) {
          this.scroll = new BScroll(this.$refs.wrapper, {
            startX: 0,
            click: true,
            scrollX: true,
            scrollY: false,
            eventPassthrough: 'vertical'
          })
        } else {
          this.scroll.refresh()
        }
      })
    }
  },
  mounted () {
    this.personScroll()
  }
}
</script>

<style lang="stylus" scoped>
  .icons
    height: 0
    padding-bottom: 20%
    overflow: hidden
    .icons-item
      width: 86px
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
        .six
          top: .18rem
          font-size: .58rem
          left: .2rem
      .icons-item-info
        width: 100%
        height: 0
        padding-bottom: 40%
        overflow: hidden
        text-align: center
        line-height: .6rem
</style>
