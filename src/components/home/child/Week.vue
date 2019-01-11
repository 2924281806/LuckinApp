<template>
    <div class="week">
      <div class="list">
        <div class="list_left">
          <img class="list-img" src="http://localhost:8080/images/huo.png" alt="">
          <span>本周热门榜单</span>
          <span class="icon iconfont">&#xe640;</span>
          <span class="total-list">全部榜单</span>
        </div>
      </div>
      <div class="wrapper">
        <div class="swiper">
          <!-- swiper -->
          <swiper :options="swiperOption">
            <swiper-slide v-for="item in RollingList" :key="item.id">
              <img class="swiper-img" :src="item.imgUrl" alt="">
              <p class="desc">{{item.desc}}</p>
              <p class="desc">
                <span class="sign">￥</span>
                <span class="num">{{item.price}}</span>
                起</p>
            </swiper-slide>
          </swiper>
        </div>
      </div>

    </div>
</template>

<script>
  export default {
    name: 'HomeWeek',
    data(){
      return {
        RollingList:[
          {
            id:'0001',
            imgUrl:'http://localhost:8080/images/r01.jpg',
            desc:'东部华侨城大峡谷',
            price:'128'
          },
          {
            id:'0002',
            imgUrl:'http://localhost:8080/images/r02.jpg',
            desc:'世界之窗',
            price:'128'
          },
          {
            id:'0003',
            imgUrl:'http://localhost:8080/images/r03.jpg',
            desc:'深圳小梅沙海洋世界',
            price:'128'
          },
          {
            id:'0004',
            imgUrl:'http://localhost:8080/images/r04.jpg',
            desc:'深圳深蓝秘境欢乐水秀',
            price:'154'
          },
          {
            id:'0005',
            imgUrl:'http://localhost:8080/images/r05.jpg',
            desc:'动植物园',
            price:'128'
          },
          {
            id:'0006',
            imgUrl:'http://localhost:8080/images/r06.jpg',
            desc:'泡温泉',
            price:'128'
          },
          {
            id:'0007',
            imgUrl:'http://localhost:8080/images/r07.jpg',
            desc:'年终大促',
            price:'128'
          },
          {
            id:'0008',
            imgUrl:'http://localhost:8080/images/r08.jpg',
            desc:'一日游',
            price:'128'
          },
          {
            id:'0009',
            imgUrl:'http://localhost:8080/images/r09.jpg',
            desc:'东部华侨城',
            price:'128'
          }
          ,
          {
            id:'0010',
            imgUrl:'http://localhost:8080/images/r10.jpg',
            desc:'溜娃儿',
            price:'128'
          }
        ],
        swiperOption: {
          slidesPerView: 3.5,
          spaceBetween: 10,
          freeMode: true
        }
      }
    }
  }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import "~styles/mixin.styl"
.list
  padding-top .2rem
  background #eee
  .list_left
    background #ffffff
    padding-top .3rem
    .list-img
      width 15px
      margin-top -.1rem
      padding-left .1rem
    .total-list
      float right
      font-size .2rem
    .icon
      float right
      font-size .2rem
      padding 0 .1rem
.wrapper
  background #eee
  padding-bottom :3%
  .swiper
    background #ffffff
    overflow :hidden
    width :100%
    height:0
    padding-bottom :45%
    /*background :#eee*/
    .swiper-img
      width 100%
      padding-top 20px
    .desc
      line-height 22px
      text-align center
      font-size .12rem
      ellipsis()
      .sign
        color: orange
      .num
        color orange
        margin-left -.1rem





</style>
