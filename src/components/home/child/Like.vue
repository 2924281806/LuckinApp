<template>
    <div class="like">
      <div class="title">
        <img class="title-img" src="http://localhost:8080/images/xin.png" alt="">
        <span class="title-desc">猜你喜欢</span>
      </div>
      <ul>
        <li class="item" v-for="item of LikeList" :key="item.id">
          <img class="item-img" :src="item.imgUrl" alt="">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-star">2222条评论</p>
            <p class="item-price">
              <span class="item-dec">￥</span>
              <span class="item-num">155</span>
              起
              <span class="item-addr">{{item.addr}}</span>
            </p>
          </div>
        </li>
      </ul>
      <div class="total">
        查看所有产品
      </div>
    </div>
</template>

<script>
   export default {
      name: 'HomeLike',
      data(){
       return {
          LikeList:[
            {
              id:'0001',
              imgUrl:'http://localhost:8080/images/r01.jpg',
              title:'东部华侨城大峡谷',
              addr:'东部华侨城大峡谷'
            },
            {
              id:'0002',
              imgUrl:'http://localhost:8080/images/r02.jpg',
              title:'阿尔卑斯滑雪场',
              addr:'世界之窗'
            },
            {
              id:'0003',
              imgUrl:'http://localhost:8080/images/r03.jpg',
              title:'青青世界',
              addr:'南山区'
            },
            {
              id:'0004',
              imgUrl:'http://localhost:8080/images/r04.jpg',
              title:'深圳深蓝秘境欢乐水秀',
              addr:'南山区'
            },
            {
              id:'0005',
              imgUrl:'http://localhost:8080/images/r05.jpg',
              title:'华侨城',
              addr:'南山区'
            }
            ,
            {
              id:'0006',
              imgUrl:'http://localhost:8080/images/r06.jpg',
              title:'深圳小梅沙海洋世界',
              addr:'小梅沙'
            }
            ,
            {
              id:'0007',
              imgUrl:'http://localhost:8080/images/r07.jpg',
              title:'深圳小梅沙海洋世界',
              addr:'小梅沙'
            }
            ,
            {
              id:'0008',
              imgUrl:'http://localhost:8080/images/r08.jpg',
              title:'深圳小梅沙海洋世界',
              addr:'小梅沙'
            }
            ,
            {
              id:'0009',
              imgUrl:'http://localhost:8080/images/r09.jpg',
              title:'深圳小梅沙海洋世界',
              addr:'小梅沙'
            }
            ,
            {
              id:'0010',
              imgUrl:'http://localhost:8080/images/r10.jpg',
              title:'深圳小梅沙海洋世界',
              addr:'小梅沙'
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
    line-height: .5rem
    margin-top :.2rem
    text-indent :.1rem
    padding-left .1rem
    .title-img
      width 15px
      margin-top :-.2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    padding-bottom .3rem
    padding-top .1rem
    border-bottom 0.01rem solid #cacaca
    .item-img
      width 1.9rem
      height: 1.9rem
      padding .1rem
    .item-info
      font-family "微软雅黑"
      flex 1
      padding .1rem
      min-width 0
      .item-title
        padding-top .2rem
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-star
        line-height .54rem
      .item-price
        line-height .4rem
        .item-dec
          color orange
        .item-num
          font-size .4rem
          color orange
          margin  -.08rem
        .item-addr
          width 30%
          float right
          text-align right
          padding-right .1rem
          ellipsis()
  .total
    line-height .8rem
    text-align center
    color: #25a4bb
    padding-bottom  -.4rem
</style>
