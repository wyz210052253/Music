<template>
    <div class="header">
      <div class="left">
        <router-link to="/"><span class="iconfont icontback">&#xe609;</span></router-link>
      </div>
      <div class="middle">
        <div class="title">遥远的她</div>
        <div class="author">张学友</div>
      </div>
      <div class="right">
        <router-link to="/"><span class="iconfont icontshare">&#xe64b;</span></router-link>
      </div>
    </div>
</template>

<script>
export default {
  name: 'PlayerHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    width: 100%
    height: 1rem
    background: #ccc
    .left
      margin-left: .2rem
      width: .8rem
      line-height: 1rem
      text-align: center
      .icontback
        color: #000
        font-size: .5rem
    .right
      margin-right: .2rem
      width: .8rem
      line-height: 1rem
      text-align: center
      .icontshare
        color: #000
        font-size: .5rem
    .middle
      flex: 1
      padding-left: .2rem
      line-height: .5rem
      .title
        font-size: .3rem
</style>
