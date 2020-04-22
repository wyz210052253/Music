<template>
    <div class="ranking">
      <div class="title">
            <div class="title-info">排行榜</div>
            <div class="title-btn border">
                查看更多
            </div>
      </div>
      <div class="item">
        <div class="item-title">硬地原创音乐榜 ></div>
        <ul class="item-list">
          <li class="item-list-box" v-for="item of list" :key="item.id">
            <div class="item-wrapper">
                <img class="item-img" :src="item.imgUrl" />
            </div>
            <div class="item-info">
              <span class="item-info-ranking">{{item.index}}</span>
              <span class="item-info-desc">{{item.title}}</span>
              <span class="item-info-author">{{item.author}}</span>
              <span class="item-info-index">新</span>
            </div>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeRanking',
  data () {
    return {
      list: [{
        id: '0001',
        index: '1',
        imgUrl: 'http://p2.music.126.net/ply41mhg-j0JQR7IvmLWOg==/109951164887544693.jpg?param=50y50&quality=100',
        title: '喉咙唱的沙哑',
        author: '- 枯木逢春'
      }, {
        id: '0002',
        index: '2',
        imgUrl: 'http://p1.music.126.net/CCUe6FkkZJynx09P5Jzjmg==/109951163925137185.jpg?param=140y140',
        title: '当音乐停止',
        author: '- 顾忠山/赵可'
      }, {
        id: '0003',
        index: '3',
        imgUrl: 'http://p2.music.126.net/lBbpT6oJoMK63afjzm8Nyw==/109951164675828957.jpg?param=140y140',
        title: 'Dawn Echo',
        author: '- 完美倒立'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .ranking >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .ranking
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 74%
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
      width: 96%
      height: 5.48rem
      margin-top: 0.04rem
      background: rgb(0,142,84)
      margin: 0 auto
      border-radius: .2rem
      .item-title
        height: .8rem
        line-height: .8rem
        padding-left: .2rem
        color: #fff
        font-size: .34rem
        font-weight: 600
      .item-list
        width: 100%
        height: 5.15rem
        margin-top: 0.04rem
        .item-list-box
          width: 100%
          height: 1.3rem
          margin-bottom: .2rem
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
            line-height: 1.3rem
            display: flex
            position: relative
            color: #fff
            .item-info-ranking
              font-size: .34rem
              padding: 0 .1rem
            .item-info-desc
              font-size: .34rem
              padding-left: .2rem
            .item-info-author
              font-size: .26rem
              padding-left: .4rem
            .item-info-index
              position: absolute
              left: 5rem

</style>
