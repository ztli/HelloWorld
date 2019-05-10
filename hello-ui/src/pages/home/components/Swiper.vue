<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" />
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts0/1810/26/3c6d0e9342a45202.jpg_r_390x260x90_b6744167.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts3/1712/78/2ead54d37575c902.jpg_r_390x260x90_9e4ab057.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/p/tts0/1712/7e/0b328627dd4bd002.jpg_r_390x260x90_a28087a8.jpg'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background : #fff
  .wrapper
    overflow : hidden
    width : 100%
    height : 0
    padding-bottom : 31.25%
    background : #eaeaea
    .swiper-img
      width : 100%
</style>
