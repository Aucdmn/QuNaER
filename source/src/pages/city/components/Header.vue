<template>
    <div class="header">
        城市选择
        <router-link to="/">
        <div class="iconfont back-icon">&#xe624;</div>
        </router-link>
    </div>
</template>

<script>
export default {
  name: 'HeaderCity'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    position relative
    height $headerHeight
    line-height $headerHeight
    background-color $bgColor
    color #ffffff
    text-align center
    .back-icon
        position absolute
        width .64rem
        top 0
        left 0
        font-size .4rem
        text-align center
        color #fff
</style>
