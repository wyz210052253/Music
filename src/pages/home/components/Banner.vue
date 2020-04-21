<template>
    <div class="wrapper">
        <swiper ref="mySwiper" :options="swiperOptions">
            <swiper-slide v-for="item of listImg" :key="item.id">
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
      },
      listImg: [
        {
          id: '0001',
          imgUrl: 'http://p1.music.126.net/7ZoV4j6XmVKd0oiA1W372w==/109951164923062522.jpg?imageView&quality=89'
        },
        {
          id: '0002',
          imgUrl: 'http://p1.music.126.net/zbK33u11twR_0M6W65tSKA==/109951164923610728.jpg?imageView&quality=89'
        },
        {
          id: '0003',
          imgUrl: 'http://p1.music.126.net/Le1EZDcpQXbM94_GmsxFLA==/109951164923454935.jpg?imageView&quality=89'
        },
        {
          id: '0004',
          imgUrl: 'http://p1.music.126.net/02fa9obQSYRMH-pGge2PQQ==/109951164923373736.jpg?imageView&quality=89'
        },
        {
          id: '0005',
          imgUrl: 'http://p1.music.126.net/oHNrQBDM06aWhEw0FZcIvg==/109951164923437470.jpg?imageView&quality=89'
        },
        {
          id: '0006',
          imgUrl: 'http://p1.music.126.net/ziZ7lSWLDCuXoaRrXpjODg==/109951164923383839.jpg?imageView&quality=89'
        },
        {
          id: '0007',
          imgUrl: 'http://p1.music.126.net/v0RoMyFXdiczgRbgIhCqkQ==/109951164923426977.jpg?imageView&quality=89'
        },
        {
          id: '0008',
          imgUrl: 'http://p1.music.126.net/boV8MzLfKAuyDA3qpICC0g==/109951164923067802.jpg?imageView&quality=89'
        },
        {
          id: '0009',
          imgUrl: 'http://p1.music.126.net/L1zqFXIsVty8U0oOSRcqIQ==/109951164923389242.jpg?imageView&quality=89'
        }
      ]
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
    .wrapper-img
      width: 100%

</style>
