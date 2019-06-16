<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList"  :key="item.id">
        <img class="item-img" src="https://imgs.qunarzz.com/sight/p0/1807/77/77570cc3ebf7d9d8a3.img.jpg_200x200_d36ff68e.jpg">
        <div class="item-info">
          <p class="info-title">{{item.titile}}</p>
          <p class="info-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1807/77/77570cc3ebf7d9d8a3.img.jpg_200x200_d36ff68e.jpg',
        titile: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1807/77/77570cc3ebf7d9d8a3.img.jpg_200x200_d36ff68e.jpg',
        titile: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1807/77/77570cc3ebf7d9d8a3.img.jpg_200x200_d36ff68e.jpg',
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
  .item
    overflow : hidden
    display : flex
    height : 1.9rem
    .item-img
      width : 1.7rem
      height : 1.7rem
      padding : .1rem
    .item-info
      flex : 1
      padding : .1rem
      min-width : 0
      .info-title
        line-height : .54rem
        font-size : .32rem
        ellipsis()
      .info-desc
        line-height : .4rem
        color : #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top : .16rem
        background : #ff9300
        padding : 0 .2rem
        border-radius : .06rem
        color : #fff
</style>
