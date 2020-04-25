<template>
    <div class="hot">
        <h3 class="hot-title">热搜榜</h3>
        <div class="hot-list" v-for="item of list" :key="item.id">
            <div class="list-left">{{item.index}}</div>
            <div class="list-right">
                <div class="list-title">
                    <div class="list-title-mian">{{item.title}}</div>
                    <div class="list-title-number">{{item.number}}</div>
                </div>
                <div class="list-desc">
                    {{item.desc}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'SearchHot',
  data () {
    return {
      list: [{
        id: '0001',
        index: '1',
        title: '中毒',
        number: '2307180',
        desc: '虐心情歌唱作人光泽用音乐让你“中毒”了!'
      }, {
        id: '0002',
        index: '2',
        title: '夏天的风',
        number: '1433807',
        desc: '单曲循环无数次 回忆杀!'
      }, {
        id: '0003',
        index: '3',
        title: '歌手当打之年',
        number: '1411550',
        desc: '决赛顺利进行， 华晨宇问鼎歌王!'
      }, {
        id: '0004',
        index: '4',
        title: '刀马旦',
        number: '1331308',
        desc: '很难想象这是2001年创作出来的歌'
      }, {
        id: '0005',
        index: '5',
        title: '与我无关',
        number: '1115647',
        desc: '还是希望你好 即使那与我无关'
      }, {
        id: '0006',
        index: '6',
        title: '歌手当打之年',
        number: '1411550',
        desc: '决赛顺利进行， 华晨宇问鼎歌王!'
      }, {
        id: '0007',
        index: '7',
        title: '刀马旦',
        number: '1331308',
        desc: '很难想象这是2001年创作出来的歌'
      }, {
        id: '0008',
        index: '8',
        title: '与我无关',
        number: '1115647',
        desc: '还是希望你好 即使那与我无关'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .hot
    margin-top: .6rem
    width: 100%
    margin-bottom: 1.2rem
    .hot-title
      line-height: .6rem
      font-size: .3rem
      font-weight: bold
      margin-left: .1rem
    .hot-list
      width: 100%
      background: #fff
      height: 1rem
      margin-bottom: .4rem
      display: flex
      .list-left
        float: left
        height: 1rem
        width: .8rem
        text-align: center
        line-height: 1rem
        font-size: .34rem
        color: red
      .list-right
        flex: 1
        position: relative
        .list-title
          line-height: .5rem
          .list-title-mian
            float: left
            font-size: .34rem
            font-weight: bold
          .list-title-number
            float: left
            position: absolute
            top: .1rem
            right: .3rem
            color: #ddd
        .list-desc
          clear: both
          color: #ccc
          line-height: .5rem

</style>
