<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    // eslint-disable-next-line no-labels,no-unused-expressions
    return {
      recommendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/1a/1a48cc20b0d6ed44a3.img.jpg',
        title: '奥林匹克塔',
        desc: '解锁京城最佳观景平台之一'
      },
      {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/1a/1a48cc20b0d6ed44a3.img.jpg',
        title: '奥林匹克塔',
        desc: '解锁京城最佳观景平台之一'
      },
      {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1804/1a/1a48cc20b0d6ed44a3.img.jpg',
        title: '奥林匹克塔',
        desc: '解锁京城最佳观景平台之一'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      min-width 0
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height  .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .2rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
