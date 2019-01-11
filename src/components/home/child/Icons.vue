<template>
    <div class="icons">

      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="(page,index) in pages" :key="index">
          <div class="icon" v-for="item in page" :key="item.id">
            <div class="icon-img">
              <img class="icon-type" :src="item.imgUrl" alt="">
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
    export default {
        name: 'HomeIcons',
        data(){
          return {
            swiperOption:{
              pagination:'.swiper-pagination',
              autoplay:0
            },
            iconList:[
              {
                id:'0001',
                imgUrl:'http://localhost:8080/images/i01.png',
                desc:'景点门票'
              },
              {
                id:'0002',
                imgUrl:'http://localhost:8080/images/i02.png',
                desc:'深圳必游'
              },
              {
                id:'0003',
                imgUrl:'http://localhost:8080/images/i03.png',
                desc:'游乐场'
              },
              {
                id:'0004',
                imgUrl:'http://localhost:8080/images/i04.png',
                desc:'海洋馆'
              },
              {
                id:'0005',
                imgUrl:'http://localhost:8080/images/i05.png',
                desc:'动植物园'
              },
              {
                id:'0006',
                imgUrl:'http://localhost:8080/images/i06.png',
                desc:'泡温泉'
              },
              {
                id:'0007',
                imgUrl:'http://localhost:8080/images/i07.gif',
                desc:'年终大促'
              },
              {
                id:'0008',
                imgUrl:'http://localhost:8080/images/i08.png',
                desc:'一日游'
              },
              {
                id:'0009',
                imgUrl:'http://localhost:8080/images/i09.png',
                desc:'东部华侨城'
              }
              ,
              {
                id:'0010',
                imgUrl:'http://localhost:8080/images/i10.png',
                desc:'溜娃儿'
              }
            ]
          }
        },
        computed:{
          pages () {
            const pages = []
            this.iconList.forEach((item,index) => {
              const page = Math.floor(index/8)
              if(!pages[page]){
                pages[page] = []
              }
              pages[page].push(item)
            })
            return pages
          }
        }
    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import "~styles/varibles.styl"
@import "~styles/mixin.styl"
.icons >>> .swiper-pagination-bullet-active
  background $bgcolor
.icons >>> .swiper-pagination
  bottom 0
.icons >>> .swiper-container
  overflow hidden
  height 0
  padding-bottom 50%
.icon
  position relative
  overflow: hidden
  float left
  width 25%
  height 0
  padding-bottom 23%
  .icon-img
    position absolute
    top:0
    right 0
    left:0
    bottom .44rem
    box-sizing border-box
    padding .05rem
    .icon-type
      height 100%
      display block
      margin 0 auto
  .icon-desc
    position absolute
    right 0
    left:0
    bottom 0
    height .44rem
    line-height .25rem
    text-align center
    color $darkTextColor
    ellipsis()
</style>
