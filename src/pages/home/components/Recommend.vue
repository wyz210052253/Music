<template>
    <div class="recommend">
        <div class="title">
            <div class="title-info">推荐歌单</div>
            <div class="title-btn border">
                查看更多
            </div>
        </div>
        <div class="wrapper" ref="wrapper">
            <div ref="list">
                <div class="content" v-for="item of list" :key='item.id'>
                  <div class="content-img">
                      <img class="item-img" :src="item.imgUrl">
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
    </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'HomeRecommend',
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
        width: 120px
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
