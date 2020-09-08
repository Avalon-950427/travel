<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(item,index) in pages" :key="index">
        <div class="icon" v-for="(pageItem, idx) in item" :key="idx">
          <div class="icon-img">
            <img class="icon-img-content" :src="pageItem.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{pageItem.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'Icons',
  data () {
    return {
      iconList: [
        {
          id: '0001',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '热门景点'
        },
        {
          id: '0002',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '滑雪季'
        },
        {
          id: '0003',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '泡温泉'
        }, {
          id: '0004',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '动植园'
        }, {
          id: '0005',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '热门景点'
        },
        {
          id: '0006',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '滑雪季'
        },
        {
          id: '0007',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '泡温泉'
        },
        {
          id: '0008',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '动植园'
        }, {
          id: '0009',
          imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=1879642513,297045869&fm=26&gp=0.jpg',
          desc: '热门景点'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
@import '~@/assets/styles/mixin.styl'
.icons >>> .swiper-container{
  height: 0
  padding-bottom: 50%
}
.icon{
  position: relative
  overflow: hidden
  float: left
  width: 25%
  height: 0
  padding-bottom: 25%
    .icon-img{
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      padding: .1rem
        .icon-img-content{
          display: block
          margin: 0 auto
          height: 100%
          ellipsis()
        }
    }
    .icon-desc{
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .44rem
      line-height: .44rem
      color: $dark-text-color
    }
}
</style>
