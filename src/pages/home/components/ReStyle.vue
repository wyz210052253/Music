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
            <li class="item-list" v-for="item of list" :key="item.id">
              <div class="item-wrapper">
                <img class="item-img" :src="item.Imgurl" />
              </div>
              <div class="item-info">
                <div class="left">
                  <div class="item-info-title">{{item.title}}</div>
                  <span :class="Styles(item.judeg)">{{item.desc}}</span>
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
  name: 'HomeReStyle',
  props: {
    list: Array
  },
  methods: {
    Styles (judeg) {
      return judeg ? 'item-info-desc' : 'item-info-desc-two'
    }
  }
}
</script>

<style lang="stylus" scoped>
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
