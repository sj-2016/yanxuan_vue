<!--识物——>为你推荐-->
<template>
  <div v-if="recommend">
    <div class="knowledgeCard" >
      <div class="textTop">为你推荐</div>
      <div  class="knowImage" v-if="recommend.recommendBanner" :style="{background:`url(${recommend.recommendBanner.picUrl})`}"><span v-if="recommend.recommendBanner">{{recommend.recommendBanner.nickname}}</span></div>
      <div class="introduce">
        <p><span v-if="recommend.recommendBanner">{{recommend.recommendBanner.subtitle}}</span><span v-if="recommend.recommendBanner">{{recommend.recommendBanner.priceInfo}}元起</span></p>
        <p v-if="recommend.recommendBanner">{{recommend.recommendBanner.title}}</p>
      </div>
    </div>
    <div class="recommend" v-for="(recommend,index) in recommend.recommends" :key="index">
      <div class="recLeft">
        <p><img src="recommend.avatar"/><span>{{recommend.nickname}}</span></p>
        <p v-if="recommend">{{recommend.title}}</p>
        <p>{{recommend.subtitle}}</p>
      </div>
      <div class="recRight"  :style="{background:`url(${recommend.picUrl})`}"><span>{{recommend.typeName}}</span></div>
    </div>
  </div>
</template>

<script>
    export default {
      props:{
        recommend:Object
      },
    }
</script>

<style scoped lang="less">
  @import '../../common/less/blend';
 .knowledgeCard{
   margin-top: .3rem;
   display: flex;
   flex-direction:column;
   align-items: center;
    .textTop{
      width:690/@rem;
      height:120/@rem;
      font-size: 32/@rem;
     text-align: center;
      line-height:120/@rem;
    }
   .knowImage{
     width:688/@rem;
     height:386/@rem;
     background:url("//yanxuan.nosdn.127.net/796f47698fe5f4f8a8e1836d294f15c3.jpg?imageView&quality=75");
     background-size:100% 100%;
     color: #333;
   }
   .introduce{
     padding:24/@rem 20/@rem 67/@rem 20/@rem;
     font-size: 36/@rem;
     width:648/@rem;
     height:94.984/@rem;
     border:1px solid #eee;
     p:last-child{
       font-size:27.999/@rem;
       color: #7f7f7f;
       margin-top: .1rem;
     }
   }
 }
  .recommend{
    width:688/@rem;
    height:271/@rem;
    border:1px solid #ececec;
    margin: 0 auto;
    margin-top: .5rem;
    display: flex;
   margin-bottom: .5rem;
    .recLeft{
      width:358.061/@rem;
      height:272/@rem;
      padding:0 30/@rem 0 20/@rem;


      p{
       img{
         width:46/@rem;
         border-radius: 50%;
         vertical-align: middle;
       }
      }
      p:first-child{
         font-size: 20/@rem;
        margin-top: .8rem;
      }
      p:nth-child(2){
        font-size: 32/@rem;
        color: #333;
        margin-top: .3rem;
      }
      p:last-child{
        font-size: 24/@rem;
        color: #7f7f7f;
        margin-top: .3rem;
      }
    }
    .recRight{
      width:279.984/@rem;
      height:272/@rem;
       background: url("//yanxuan.nosdn.127.net/f8c462f078d259736ce2f9584df487b6.jpg");
      background-size:100% 100%!important;
      overflow: hidden;
      text-overflow:ellipsis;
      white-space: nowrap;
      span{
        display: inline-block;
        background: #fff;
        border-radius: .3rem;
        font-size: 24/@rem;
        width:167/@rem;
        height:34/@rem;
        margin-left: .3rem;
        text-align: center;
      }
    }
  }
</style>
