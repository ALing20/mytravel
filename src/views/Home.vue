<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from '../components/Header.vue'
import HomeSwiper from '../components/swiper.vue'
import HomeIcons from '../components/Icons.vue'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons
  }
}
</script>

<style lang="less">
  body {
    background-color: #f5f5f5;
  }
</style>
