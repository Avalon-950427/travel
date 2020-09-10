<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alphabet></city-alphabet>
  </div>
</template>

<script>
import CityHeader from '@/views/city/components/CityHeader.vue'
import CitySearch from '@/views/city/components/Search.vue'
import CityList from '@/views/city/components/List.vue'
import CityAlphabet from '@/views/city/components/Alphabet.vue'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  }
}
</script>

<style lang="stylus" scoped>

</style>
