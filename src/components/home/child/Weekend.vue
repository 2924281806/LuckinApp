<template>
  <div class="like">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of LikeList" :key="item.id">
        <div class="item-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'HomeWeekend',
    data(){
      return {
        LikeList:[
          {
            id:'0001',
            imgUrl:'http://localhost:8080/images/w01.jpg',
            title:'深圳必打卡',
            desc:'来到深圳，你必须要来这里签到'
          },
          {
            id:'0002',
            imgUrl:'http://localhost:8080/images/w02.jpg',
            title:'粤东泡汤好去处',
            desc:'来到深圳，你必须要来这里签到'
          },
          {
            id:'0003',
            imgUrl:'http://localhost:8080/images/w03.jpg',
            title:'东部华侨城温泉',
            desc:'来到深圳，你必须要来这里签到'
          },
          {
            id:'0004',
            imgUrl:'http://localhost:8080/images/w04.jpg',
            title:'深圳小梅沙海洋世界',
            desc:'来到深圳，你必须要来这里签到'
          },
          {
            id:'0005',
            imgUrl:'http://localhost:8080/images/w05.jpg',
            title:'深圳小梅沙海洋世界',
            desc:'来到深圳，你必须要来这里签到,你必须要来这里签到,你必须要来这里签到,你必须要来这里签到'
          }
        ]
      }
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
  @import "~styles/mixin.styl"
  .like
    width 100%
    .title
      line-height: .7rem
      text-indent :.1rem
      padding-left .1rem
      padding-top .1rem
      background #f0f0f0
    .item-wrapper
      overflow hidden
      height 0
      padding-bottom 33.9%
      padding-top .1rem
      background #f0f0f0
      .item-img
        width 100%
    .item-info
      font-family "微软雅黑"
      padding .1rem
      .item-title
        padding-top .1rem
        line-height .4rem
        font-size .32rem
        font-size 14px
        ellipsis()
        width 30%
      .item-desc
        line-height .4rem
        font-size 12px
        padding-bottom .1rem
        ellipsis()
        width 80%

</style>
