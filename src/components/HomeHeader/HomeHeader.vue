<!--首页头部-->
<template>
  <div class="homeHeader">
    <div class="text">网易严选</div>
    <div class="icon"><i class="iconfont icon-fangdajing"></i><span>搜索商品, 共10719款好物</span></div>
  </div>
</template>

<script>

  export default {

    mounted () {

    }
  }
</script>

<style scoped lang="less">
  @import '../../common/less/blend';
  .homeHeader{
    width:690/@rem;
    height:55.969/@rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding:16/@rem 30/@rem;

    .text{
      font-family:'楷体';
      font-size: 35/@rem;
    }
    .icon{
      width:532/@rem;
      height:56/@rem;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #ededed;
      border-radius:.1rem ;
      i{
        font-size: 32/@rem;
        margin-right: 10/@rem;
      }
      span{
        color: #666;
        font-size: 27.9998/@rem;
      }
    }
  }
</style>
