<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-image" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 4000
      },
      swiperList: [{
        id: '001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/d52e15a5769b90dc1fc8ad15b093d70f.jpg_750x200_71f1c317.jpg'
      }, {
        id: '002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/eb3fdb7ff86de0160cafe76b6a6a8ee3.jpg_750x200_e6930e5c.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #ffffff
  .wrapper
    overflow hidden
    height 0
    width 100%
    padding-bottom 26.7%
    background #cacaca
    .swiper-image
      width 100%
</style>
