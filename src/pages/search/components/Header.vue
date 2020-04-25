<template>
    <div class="header">
        <div class="left">
            <router-link to="/"><span class="iconfont back">&#xe609;</span></router-link>
        </div>
        <div class="middle">
            <input type="text" placeholder="Alan Walker" class="input-text" ref="input">
        </div>
        <div class="right">
            <router-link to="/"><span class="iconfont song">&#xe603;</span></router-link>
        </div>
    </div>
</template>

<script>
export default {
  name: 'SearchHeader',
  methods: {
    inputfocus () {
      this.$refs.input.focus()
    }
  },
  mounted () {
    this.inputfocus()
  }
}
</script>

<style lang="stylus" scoped>
  .header
    width: 100%
    height: 1rem
    line-height: 1rem
    background: #fff
    overflow: hidden
    display: flex
    .left
      float: left
      margin: 0 .2rem
      width: .8rem
      text-align: center
      .back
        font-size: .5rem
        color: #000
    .middle
      flex: 1
      .input-text
        width: 90%
        height: 60%
        font-size: .30rem
        padding: 0 .2rem
        border-bottom: 1px solid #ccc
    .right
      margin: 0 .2rem
      .song
        font-size: .6rem
        color: #000
</style>
