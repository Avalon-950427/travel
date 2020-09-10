<template>
  <ul class="list">
    <li class="item" v-for="(value,key) in cities" :key="key">{{key}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityHeader',
  props: {
    cities: {
      type: Object,
      default: function () {
        return {}
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'
.list
  display: flex
  flex-direction: column
  justify-content center
  position absolute
  top: 1.58rem
  right: 0
  bottom: 0
  width: .4rem
  .item
    line-height: .4rem
    text-align: center
    color: $bg-color
</style>
