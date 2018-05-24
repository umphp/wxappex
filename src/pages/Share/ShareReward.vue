<template lang="pug">
#shareReward
  .redbg(style="background-image: url('/static/assets/fenxiang_bj@2x.png") 
    div 恭喜老板，封包成功！
    div 预计将带来20条全新的人脉！
    div 助力交友，系统多加5元！
    .redimg 
      image(src="/static/assets/share/hongbao@2x.png")
  .tip （关注XXX公众号随时接收红包消息！）
  .btn 分享给朋友
  .btn.pengyouquan 分享到朋友圈

</template>
<style lang="less">
  #shareReward {
    .redbg {    
      z-index: 2;  
      position: relative;
      width: 375px;
      height: 277px;
      background-size: 375px 277px;
      text-align: center;
      div:first-of-type {
        color: #ffffff;
        height: 40px;
        line-height: 40px;
        padding-top: 20px;
      }
      div:nth-child(2) {
        color: #FDF558;
        font-size: 15px;
      }
      div:nth-child(3) {
        position: relative;
        color: #666666;
        background-color: #FFF3E1;
        width: 250px;
        margin: 0 auto;
        height: 40px;
        line-height: 40px;
        margin-top: 20px;
        border-radius: 40px;
        font-size: 16px;
        z-index: 3;
      }
      .redimg {
        position: relative;
        z-index: 2;
        image {
          position: absolute;
          width: 230px;
          height: 130px;
          margin: 0 auto;
          margin-left: -115px;
          top: -20px;
          z-index: 2;
        }        
      }
    }
    .tip {
      color: #FF4B00;
      text-align: center;
      font-size: 15px;
      height: 20;
      line-height: 20px;
      margin-top: 50px;
    }
    .btn {
      background-color: #FF4B00;
      color: #ffffff;
      width: 300px;
      height: 45px;
      line-height: 45px;
      margin: 0 auto;
      border-radius: 40px;
      text-align: center;
      font-size: 16px;
      margin-top: 16px;
    }
    .pengyouquan {
      background-color: #F7D4CB;
      border: 1px solid #FF4B00;
      color: #FF4B00;
    }
  }
</style>
<script>
export default {
}
</script>


