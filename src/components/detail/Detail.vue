<template>
    <div class="detail">
      <detail-banner :sightName="sightName" :bannerImg="bannerImg" :galleryImgs="galleryImgs"></detail-banner>
      <detail-header></detail-header>
      <detail-sort></detail-sort>
      <detail-list :list="categoryList"></detail-list>

    </div>
</template>

<script>
  import DetailHeader from './child/Header.vue'
  import DetailBanner from './child/Banner.vue'
  import DetailList from './child/List.vue'
  import DetailSort from './child/Sort.vue'

  import axios from 'axios'
    export default {
        name: 'Detail',
        components:{
          'detail-header':DetailHeader,
          'detail-banner':DetailBanner,
          'detail-list':DetailList,
          'detail-sort':DetailSort
        },
        data(){
          return{
            sightName: '',
            bannerImg: '',
            galleryImgs: [],
            categoryList: []
          }
        },
        methods:{
          getDetailInfo(){
            axios.get('/api/detail.json',{
              params:{
                id:this.$route.params.id
              }
            }).then(this.handleGetDataSucc)
          },
          handleGetDataSucc(res){
            res = res.data
            if(res.ret && res.data){
              const data = res.data
              this.sightName = data.sightName
              this.bannerImg = data.bannerImg
              this.galleryImgs = data.galleryImgs
              this.categoryList = data.categoryList
            }
          }

        },
        mounted(){
          this.getDetailInfo()

        }

    }
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
.detail
  height 50rem
</style>
