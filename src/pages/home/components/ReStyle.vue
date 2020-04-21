<template>
    <div class="restyle">
        <div class="title">
            <div class="title-info">风格推荐</div>
            <div class="title-btn border">
                播放全部
            </div>
        </div>
        <ul>
            <li>11111</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeReStyle'
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
    padding-bottom: 50%
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
</style>
