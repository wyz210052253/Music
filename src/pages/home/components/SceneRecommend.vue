<template>
   <div class="scene">
       <div class="title">
            <div class="title-info">场景推荐</div>
            <div class="title-btn border">
                查看更多
            </div>
        </div>
        <div class="wrapper">
            <div class="content" v-for="item of list" :key='item.id'>
                <div class="content-img">
                    <img class="item-img" :src="item.url">
                    <div class="item-img-play">
                        <span class="iconfont">&#xe769;</span>{{item.play}}
                    </div>
                    <span class="item-img-title">{{item.text}}</span>
                </div>
                <p class="content-desc">
                    {{item.desc}}
                </p>
            </div>
        </div>
   </div>
</template>

<script>
export default {
  name: 'HomeScene',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  .scene >>> .border::before
    border-color: #ccc
    border-radius:  1rem
  .scene
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
        width: 25%
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
          .item-img-title
            position: absolute
            bottom: .5rem
            left: 0
            color: #fff
            font-size: .30rem
            font-weight: 600
            display: block
            width: 100%
            text-align: center
        .content-desc
          width: 100%
          padding: 0 .1rem
          word-wrap: wrap
          box-sizing: border-box
          line-height: .36rem
          text-align: center
          font-size: .20rem
</style>
