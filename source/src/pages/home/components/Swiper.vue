<template>
    <div class="wrapper">
      <swiper ref="mySwiper" :options="swiperOptions">
          <swiper-slide v-for="item of list" :key="item.id">
            <img :src="item.imgUrl" class="swiper-img">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        loop: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      }
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
