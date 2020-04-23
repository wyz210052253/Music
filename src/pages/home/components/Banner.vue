<template>
    <div class="wrapper">
        <swiper ref="mySwiper" :options="swiperOptions" v-if="showSwiper">
            <swiper-slide v-for="item of list" :key="item.id">
                <img class="wrapper-img" :src="item.imgUrl">
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeBanner',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000,
        speed: 1500
      }
    }
  },
  props: {
    list: Array
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: red
  .wrapper
    width: 94%
    height: 0
    overflow: hidden
    padding-bottom: 37.8%
    background: #eeeeee
    border-radius: .1rem
    margin: .2rem auto
    margin-top: 1rem
    .wrapper-img
      width: 100%

</style>
