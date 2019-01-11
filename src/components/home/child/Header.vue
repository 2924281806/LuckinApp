<template>
    <div class="header">
      <div class="header-left">城市
        <span class="iconfont arrow_icon">&#xe64a;</span>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题</div>
      <div class="header-right">
        <span class="iconfont info_icon">&#xe62f;</span>
      </div>
    </div>
</template>

<script>
    export default {
        name: 'HomeHeader',
        data(){
        }
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import "~styles/varibles.styl"
.header
  line-height .86rem
  display flex
  background $bgcolor
  color #ffffff
  .header-left
    width 1.24rem
    float left
    text-align center
    .arrow_icon
      font-size .01rem
      margin-left -.04rem
  .header-input
    flex 1
    height .64rem
    line-height .64rem
    margin-top .12rem
    margin-right  .2rem
    padding-left .2rem
    background #ffffff
    border-radius .08rem
    color #ccc
  .header-right
    width .64rem
    float right
    .info_icon
      text-align center
      font-size .5rem

</style>
