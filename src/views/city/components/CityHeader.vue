<template>
  <div class="header">
    城市选择
    <div class="iconfont header-back" @click="back">&#xe624;</div>
  </div>
</template>

<script>
export default {
  name: 'cityHeader',
  methods: {
    back () {
      this.$router.back()
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
.header
  overflow: hidden
  position: relative
  height: .86rem
  line-height: .86rem
  text-align: center
  color: white
  background: $bg-color
  .header-back
    position: absolute
    top: 0
    left: 0
    width: .64rem
    text-align: center
    font-size: .4rem
</style>
