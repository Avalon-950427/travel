<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" v-for="(item,index) in recommendList" :key="index">
        <img class="item-img" :src="item.img" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
      recommendList: [
        {
          id: '0001',
          img: '/imgs/swiper1.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }, {
          id: '0001',
          img: '/imgs/swiper1.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }, {
          id: '0001',
          img: '/imgs/swiper1.jpg',
          title: '大连生涯海洋公园',
          desc: '烂漫大连首站,浪漫的海洋主题乐园'
        }, {
          id: '0001',
          img: '/imgs/swiper1.jpg',
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

.item
  overflow: hidden
  display: flex
  height: 1.9rem
  .item-img
    width: 1.7rem
    heigth: 1.7rem
    padding: .1rem
  .item-info
    flex: 1
    padding: .1rem
    text-align: left
    min-width: 0
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .54rem
      color: #ccc
      ellipsis()
    .item-button
      margin-top: .16rem
      line-height: .44rem
      background: #ff9300
      padding: 0 .2rem
      border-radius: .06rem
      color: #fff
</style>
