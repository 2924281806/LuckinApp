<template>
    <div class="app">
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <home-location></home-location>
      <home-week></home-week>
      <home-like></home-like>
      <home-weekend></home-weekend>
    </div>
</template>

<script>
  import HomeHeader from  './child/Header.vue'
  import HomeSwiper from  './child/Swiper.vue'
  import HomeIcons from  './child/Icons.vue'
  import HomeLocation from  './child/Location.vue'
  import HomeWeek from  './child/Week.vue'
  import HomeLike from  './child/Like.vue'
  import HomeWeekend from  './child/Weekend.vue'
    export default {
        name: 'App',
        components:{
          'home-header':HomeHeader,
          'home-swiper':HomeSwiper,
          'home-icons':HomeIcons,
          'home-location':HomeLocation,
          'home-week':HomeWeek,
          'home-like':HomeLike,
          'home-weekend':HomeWeekend
        }
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">

</style>
