<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of WeekendList"  :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img"
               src="https://imgs.qunarzz.com/sight/p0/1503/4a/4a2ba4bfc1d8d25b.water.jpg_640x276_86819a14.jpg">
        </div>
        <div class="item-info">
          <p class="info-title">{{item.titile}}</p>
          <p class="info-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      WeekendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1503/4a/4a2ba4bfc1d8d25b.water.jpg_640x276_86819a14.jpg',
        titile: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1503/4a/4a2ba4bfc1d8d25b.water.jpg_640x276_86819a14.jpg',
        titile: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1503/4a/4a2ba4bfc1d8d25b.water.jpg_640x276_86819a14.jpg',
        titile: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~@/assets/styles/mixins.styl"
  .title
    margin-top : .2rem
    line-height : .8rem
    background : #eee
    text-indent : .2rem
  .item-img-wrapper
    overflow : hidden
    height : 0
    padding-bottom : 33.9%
    .item-img
      width : 100%
  .item-info
    padding : .1rem
    .info-title
      line-height : .54rem
      font-size : .32rem
      ellipsis()
    .info-desc
      line-height : .4rem
      color : #ccc
      ellipsis()
</style>
