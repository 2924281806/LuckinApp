<template>
    <div class="header">
      <router-link  to="/city">
        <div class="header-left">
          {{this.city}}
          <span class="iconfont arrow_icon">&#xe64a;</span>
        </div>
      </router-link>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
      </div>
      <div class="header-right">
        <span class="iconfont info_icon">&#xe62f;</span>
      </div>
    </div>
</template>

<script>
    import { mapState } from 'vuex'
    export default {
        name: 'HomeHeader',
        computed:{
          ...mapState(['city'])
        }
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import "~styles/varibles.styl"
.header
  display block
  line-height .86rem
  display flex
  background $bgColor
  color #ffffff
  .header-left
    min-width 1.04rem
    padding 0 .1rem
    float left
    text-align center
    color white
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
