<template>
    <div class="broadcat">
        <div class="title">
            <div class="title-info">电台推荐</div>
            <div class="title-btn border">
                查看更多
            </div>
        </div>
        <div class="wrapper" ref="wrapper">
            <div ref="list">
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
    </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'HomeBroadcast',
  props: {
    list: Array
  },
  mounted () {
    this.$nextTick(() => {
      let width = 6 * 120
      this.$refs.list.style.width = width + 'px'
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
    })
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
        width: 100px
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
