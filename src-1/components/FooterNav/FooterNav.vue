<template>
  <div class="footer">
    <div class="footer-home">
      <a href="javascript:;" @click.prevent="$router.replace('/shopMain')">
        <div class="footer-class-icon icon-home" :class="{active: $route.path==='/shopMain'}"></div>
        <span>首页</span>
      </a>
    </div>
    <div class="footer-topic">
      <a href="javascript:;" @click.prevent="$router.replace('/shopLooks')">
        <div class="footer-class-icon icon-topic" :class="{active: $route.path==='/shopLooks'}"></div>
        <span>识物</span>
      </a>
    </div>
    <div class="footer-class">
      <a href="javascript:;" @click.prevent="$router.replace('/shopLists')">
        <div class="footer-class-icon icon-class" :class="{active: $route.path==='/shopLists'}"></div>
        <span>分类</span>
      </a>
    </div>
    <div class="footer-cart">
      <a href="javascript:;" @click.prevent="$router.replace('/shopChart')">
        <div class="footer-class-icon icon-cart" :class="{active: $route.path==='/shopChart'}"></div>
        <span>购物车</span>
      </a>
    </div>
    <div class="footer-person">
      <a href="javascript:;" @click.prevent="$router.replace('/personCenter')">
        <div class="footer-class-icon icon-person" :class="{active: $route.path==='/personCenter'}"></div>
        <span>个人</span>
      </a>
    </div>
  </div>
</template>

<script>
  export default {}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../../common/stylus/mixins.styl"
  .footer
    top-border-1px(#eee)
    justify-content space-around
    position fixed
    z-index 5
    left 0
    bottom 0
    width 100%
    height 49px
    background-color #fafafa
    display flex
    align-items center
    >div
      font-size 13px
      color black
      >a
        display flex
        flex-direction column
        align-items center
        cursor pointer
        >span
          margin-top 3px
        .footer-class-icon
          width: 20px
          height: 20px
          background-image url("./image/foot.png")
          background-size 20px
          background-repeat no-repeat
        .icon-home
          background-position -1px -125px
          &.active
            background-position -1px -99px
        .icon-topic
          background-position -1px -176px
          &.active
            background-position -1px -150px
        .icon-class
          background-position -1px -76px
          &.active
            background-position -1px -50px
        .icon-cart
          background-position -1px -26px
          &.active
            background-position -1px 0px
        .icon-person
          background-position -1px -226px
          &.active
            background-position -1px -200px
</style>
