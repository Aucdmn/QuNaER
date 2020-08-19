<template>
    <div class="wrapper">
      <swiper ref="mySwiper" :options="swiperOptions">
          <swiper-slide v-for="item of swiperList" :key="item.id">
            <img :src="item.imgUrl" class="swiper-img">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        loop: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg'
      },
      {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/c0a60fa20379efa4f02ce527a680dc1b.jpeg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff !important
  .wrapper
    width 100%
    overflow hidden
    height 0
    padding-bottom 31.25%
    .swiper-img
      width: 100%

</style>
