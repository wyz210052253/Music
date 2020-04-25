<template>
    <div class="history">
        <div class="header">
            <h3 class="header-title">历史记录</h3>
            <span class="iconfont header-delete">&#xe607;</span>
        </div>
        <div class="main">
            <span class="list" v-for="item of list" :key="item.id">{{item.desc}}</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'SearchHistory',
  data () {
    return {
      list: [{
        id: '0001',
        desc: '登峰造极'
      }, {
        id: '0002',
        desc: '逝去日子'
      }, {
        id: '0003',
        desc: '遥远的她'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .history
    width: 96%
    height: 0
    overflow :hidden
    padding-bottom: 20%
    background: #fff
    margin: .4rem auto
    .header
      width: 100%
      height: .6rem
      .header-title
        float: left
        line-height: .6rem
        font-size: .3rem
        font-weight: bold
        margin-left: .1rem
      .header-delete
        float: right
        line-height: .6rem
        margin-right: .2rem
        font-size: .4rem
        color: #ccc
    .main
      width: 100%
      margin-top: .3rem
      margin-left: .1rem
      .list
        background: #eee
        float: left
        height: .5rem
        line-height: .5rem
        padding: .1rem .3rem
        border-radius: .4rem
        font-size: .28rem
        margin-right: .2rem
</style>
