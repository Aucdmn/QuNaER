<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img
        class="banner-img"
        src="https://img1.qunarzz.com/sight/p0/201311/25/581435d34c44340438a51592a21a2799.jpg_256x160_c937ee0e.jpg"
      >
      <div class="banner-info">
        <div class="banner-title">
          贵州安顺黄果树大瀑布(AAAAA级景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#59054;</span>
          39
        </div>
      </div>
    </div>
    <common-gallery :imgs="imgs" v-show="showGallery"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  methods: {
    handleBannerClick () {
      this.showGallery = true
    }
  },
  data () {
    return {
      showGallery: false,
      imgs: ['https://imgs.qunarzz.com/vs_ceph_vs_tts/b2c33082-d525-4a3b-88c1-1b592b1f8632.jpg_r_390x260x95_d87fa97d.jpg',
        'https://imgs.qunarzz.com/vs_ceph_vs_tts/aa0e51bd-1997-49c1-9d1d-d92e44adfff8.jpg_r_390x260x95_3dcd3945.jpg']
    }
  },
  components: {
    CommonGallery
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    width 100%
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
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8))
      .banner-title
        flex 1
        font-size .26rem
        padding 0 .2rem
      .banner-number
        height .26rem
        line-height .26rem
        margin-top .17rem
        padding 0 .4rem
        border-radius .2rem
        background rgba(0, 0, 0, .8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
