<template>
    <div class="player">
        <div class="title">
            <div class="title-info">大家都在听</div>
            <div class="title-btn border">
                <span class="iconfont player-btn">&#xe62b;</span>
                播放全部
            </div>
        </div>
        <ul class="item">
             <swiper :options="swiperOptions">
               <swiper-slide v-for="(page, index) of pages" :key="index">
                  <li class="item-list" v-for="item of page" :key="item.id">
                    <div class="item-wrapper">
                      <img class="item-img" :src="item.imgUrl" />
                    </div>
                    <div class="item-info">
                      <div class="left">
                        <div class="item-info-title">{{item.title}}</div>
                        <div class="item-info-desc">
                          <span class="item-desc-left">SQ</span>
                          <span class="item-desc-right">{{item.desc}}</span>
                        </div>
                      </div>
                      <div class="item-player border">
                        <span class="iconfont">&#xe62b;</span>
                      </div>
                    </div>
                  </li>
               </swiper-slide>
             </swiper>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomePlayer',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 3)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  .player >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .player
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
