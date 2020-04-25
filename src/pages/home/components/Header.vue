<template>
    <div class="header">
      <div class="header-left">
        <span class="iconfont icon-list">&#xe650;</span>
      </div>
      <div class="header-middle">
        <ul>
          <router-link  to="/" class="header-middle-title">我的</router-link>
          <router-link  to="/" class="header-middle-title">发现</router-link>
          <router-link  to="/" class="header-middle-title">云村</router-link>
          <router-link  to="/" class="header-middle-title">视频</router-link>
        </ul>
      </div>
      <div class="header-right">
        <router-link to="/search"><span class="iconfont iconfont-search">&#xe612;</span></router-link>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    color: #333
    height: .8rem
    line-height: .8rem
    display: flex
    .header-left
      width: .64rem
      float: left
      text-align: center
      margin: 0 .6rem 0 .2rem
      .icon-list
        font-size: .48rem
    .header-middle
      flex: 1
      margin-left: .2rem
      font-size: .30rem
      .header-middle-title
        float: left
        margin: 0 .3rem
        color: #000
    .header-right
      width: .64rem
      text-align: center
      margin-right: .2rem
      .iconfont-search
        font-size: .48rem
        color: #000
</style>
