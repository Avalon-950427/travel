<template>
  <div class="wrapper">
     <!-- ref="mySwiper" @someSwiperEvent="callback" -->
    <swiper :options="swiperOption">
      <swiper-slide v-for="(item,index) in swiperList" :key="index">
        <img class="swiper-img" :src="item" alt="">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <!-- <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
      <div class="swiper-scrollbar" slot="scrollbar"></div> -->
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: ['/imgs/swiper1.jpg', '/imgs/swiper2.jpg']
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active{
    background: white !important;
  }
.wrapper{
  overflow: hidden
  width: 100%
  height: 4rem
  .swiper-img{
    width: 100%;
    height: 4rem;
  }
}
</style>
