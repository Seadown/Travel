<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        src="http://himg1.qunarzz.com/imgs/201907/09/C.AuJG8gzjgDOKqH06z1024.jpg"
      />
      <div class="banner-info">
        <div class="banner-title">北京雅山小筑民宿</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe6df;</span>
          53
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClick"
    >
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['https://himg1.qunarzz.com/imgs/201907/09/C.-jGDMRjxUJ5oAGk6R480.jpg',
        'https://himg1.qunarzz.com/imgs/201907/09/C.AuJG8gzjgDOKqH06z480.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClick () {
      this.showGallary = false
    }
  },
  components: {CommonGallary}
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        margin-top .14rem
        padding 0 .4rem
        line-height .32rem
        height .32rem
        border-radius .2rem
        background rgba(0, 0, 0, .8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
