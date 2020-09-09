<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" v-for="(item,index) in recommendList" :key="index">
        <div class="item-img-wrap">
          <img class="item-img" :src="item.img" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
      recommendList: [
        {
          id: '0001',
          img: '/imgs/swiper1.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }, {
          id: '0001',
          img: '/imgs/swiper2.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }, {
          id: '0001',
          img: '/imgs/swiper1.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }, {
          id: '0001',
          img: '/imgs/swiper2.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/mixin.styl'
.title
  margin-top: .2rem
  line-height: .8rem
  background: #eeeeee
  text-indent: .2rem
  text-align: left
.item-img-wrap
  overflow: hidden
  height: 1.7rem
  .item-img
    width: 100%
    // padding: .1rem
    // box-sizing: border-box
.item-info
  padding: .1rem
  text-align: left
  min-width: 0
  box-sizing: border-box
  .item-title
    line-height: .54rem
    font-size: .32rem
    ellipsis()
  .item-desc
    line-height: .54rem
    color: #ccc
    ellipsis()
</style>
