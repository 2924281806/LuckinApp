<template>
    <div class="location">
      <div class="location-left">
        <span class="iconfont">&#xe63f;</span>
        深圳
      </div>
      <div class="location-right">
        <span class="iconfont">&#xe602;</span>
        必游榜单
      </div>
    </div>
</template>

<script>
    export default {
        name: 'HomeLocation'
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
.location
  height 0
  padding-bottom 10%
  .location-left
    float left
    width 50%
    padding-bottom: 10%
    text-align center
    box-sizing border-box
    padding .23rem
    border-top 0.01rem solid #cacaca
    border-right 0.01rem solid #cacaca
  .location-right
    float right
    width 50%
    padding-bottom: 10%
    text-align center
    box-sizing border-box
    padding .23rem
    border-top 0.01rem solid #cacaca
</style>
