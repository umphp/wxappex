<template lang="pug">
#sendCard
  .tip 红包金额越大，您的名片将会被推送给越多人哦！
    i.tip-con 
  .inputbg 
    .inputcontent 
      div 红包金额
      div 
        input(placeholder='0.00')
        span 元
    .inputcontent.marginTop.linqurenshu 
      div 领取人数
      div 
        input(placeholder='0')
  .showsum ￥
    span 0.00
  .btn-send 塞红包进名片
  .tipnext 
    span 您可以在
    span.tipstyle 人脉圈>好友圈
    span 与领取红包的朋友聊天！

</template>
<style lang="less">
page{
background-color:#F6F6F6;
height:100%;
}
#sendCard {
  .tip {
    position: relative;
    color: #FD9526;
    font-size: 13px;
    padding-left: 40px;
    background-color: #FFF4EC;
    height: 40px;
    line-height: 40px;
  }
  .tip-con {
    position: absolute;
    top: 50%;
    margin-top: -7.5px;
    left: 20px;
    // background-image: url('../../../resource/tishi@2x.png');
    background-size: cover;
    height: 15px;
    width: 15px;
  }
  .inputbg { 
    padding: 20px;
    background-color: #ffffff;
    color: #000000;
    font-size: 16px;
  }
  .inputcontent {
    display: flex;
    background-color: #F3F5F9;
    line-height: 50px;
    height: 50px;
    padding-left: 10px;
    div:first-of-type {
      width: 30%;
    }
    div:last-of-type {
      position: relative;
      width: 70%;
      text-align: right;
      padding-right: 30px;
      height: 50px;
      line-height: 50px;
      input { 
        width: auto;
        display: inline-block;
        text-align: right;
        line-height: 50px;
        height: 50px;
      }
      span {
        position: absolute;
        right: 10px;
      }
    }
  }
  .marginTop {
    margin-top: 10px;
  }
  .showsum {
    text-align: center;
    height: 100px;
    line-height: 100px;
    font-size: 15px;
    span {
      font-size: 25px;
    }
  }
  .btn-send {
    width: 328px;
    height: 50px;
    line-height: 50px;
    background-color: #FF4B00;
    color: #ffffff;
    margin: 0 auto;
    text-align: center;
    border-radius: 30px;

  }
  .tipnext {
    height: 30px;
    line-height: 30px;
    font-size: 12px;
    text-align: center;
    color: #999999;
    .tipstyle {
      color: #FF4B00;
    }
  }
  .linqurenshu {
    div:last-of-type { 
      padding-right: 10px;
    }
  }
}
</style>
<script>

</script>


