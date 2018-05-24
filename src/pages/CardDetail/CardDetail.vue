<template lang="pug">
#CardDetail
  div.redRecord(style="background-image: url('/static/assets/hongbao_bj@3x.png'")
    .touxiang
      image(src="/static/assets/1024_1024.png")
    .redDetail
      p 陈三元(老板)
      p 做XX行业的朋友来认识一下
      p ￥100
  .redRecordSum 还有10个未领取哦！
  .detail 
    .detailbg 
      div 
        image(src="/static/assets/1024_1024.png") 
      .detaildiv 
        p.detailp
          span 陈三元（老板） 
          span 广州XXXX科技有限公司
          
        p(class='detailp timeMoney')
          span 2018.4.20 12:12:12
          span 20.00元
  .detail 
    .detailbg 
      div 
        image(src="/static/assets/1024_1024.png") 
      .detaildiv
        p.detailp
          span 陈三元（老板） 
          span 广州XXXX科技有限公司
          
        p.detailp.timeMoney
          span 2018.4.20 12:12:12
          span 20.00元
  .detail 
    .detailbg 
      div 
        image(src="/static/assets/1024_1024.png") 
      .detaildiv 
        p.detailp
          span 陈三元（老板） 
          span 广州XXXX科技有限公司
          
        p.detailp.timeMoney
          span 2018.4.20 12:12:12
          span 20.00元


</template>
<style lang="less">  
page{
    background-color:#F6F6F6;
    height:100%;
}
#CardDetail {

.redRecord {
  position: relative;
  width: 375px;
  height: 210px;
  background-size: 375px 110px;
  background-position: 0 -40px;
  background-repeat: no-repeat;
  background-color: #fb3955;
  padding-top: 23px;
  .touxiang{    
    width: 70px;
    height: 70px;
    margin: 0 auto;
    border-radius: 50%;
    image {
      width: 100%;
      height: 100%;
      border-radius: 50%;
    }
  }
  .redDetail {
    color: #ffffff;
    text-align: center;
    p:nth-child(1){
      margin-top: 10px;
      font-size: 20px;
    }
    p:nth-child(2) {
      font-size: 16px;
      margin-top: 10px;
    }
    p:nth-child(3) {
      font-size: 40px;
      color: #FFD266;
      margin-top: 15px;
    }

  }
}
.redRecordSum {
  color: #333333;
  font-size: 16px;
  text-align: center;
  height: 40px;
  line-height: 40px;
}
.detaildiv {
  display: flex;
  flex: 1;
}
.detail {
  padding: 15px;
  width: 330px;
  height: 50px;
  background-color: #ffffff;
  margin: 0 auto;
}
.detailbg {
  border-bottom: 1px solid #EEEEEE;
  padding-bottom: 14px;
  display: flex;
  font-size: 14px;
  div:nth-child(1) {
    flex: 0 0 50px;
    height: 50px;
    border-radius: 50%;
    image {
      width: 100%;
      height: 100%;
      border-radius: 50%;
    }
  }
  .detailp {
    flex: 1;
    display: flex;
    justify-content: center;
    font-size: 12px;
    flex-direction: column;
    padding-left: 10px;
    span:nth-child(2){
      padding-top: 10px;
    }
  }
  .timeMoney {
    text-align: right;
    span:nth-child(1) {
      color: #999999;
    }
    span:nth-child(2) {
      color: #FF4B00;
    }
  }
}
.border {
  border-bottom: 1px solid #ccc;
}
}

</style>
<script>

</script>


