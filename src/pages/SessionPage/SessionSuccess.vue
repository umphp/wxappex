<template lang='pug'>
#SessionSuccess
  .mesdiv
    div 
      image(src="/static/assets/1024_1024.png")
    div 
      span.name 陈三元 
        span.position (总经理)
      span 广东易上云计算机股份有限公司
    div 
      image(src='/static/assets/shouji@2x.png')
      <span>交换手机号</span>
  .showmsg 
    .time 14:14
    .sessionMsg 
      div.msgp 
        p
          image(src='/static/assets/shenqing@2x.png') 
          span 您已发起交换手机号申请        
        p.wait
          span  （等待对方确认）
      div.sendimg
        div
          image(src="/static/assets/1024_1024.png")
    .isagree 
      span 对方已同意您的申请
    .recevidebg
      .recevide
        .recevidemsg
          p 陈三元
          p 
            image(src="/static/assets/gongsi@2x.png") 
            span 广东易上云股份有限公司
          p 
            image(src="/static/assets/zhiwei@2x.png")  
            span CEO
          p
            image(src="/static/assets/shoujihao@2x.png")  
            span 1382982098
        .recevideimg 
          div
            image(src="/static/assets/1024_1024.png")
      .recevideTip 有物流资源的欢迎找我哦！
    .changePhone 
      span 已交换手机号
</template>
<style lang='less'>
#SessionSuccess {
  .mesdiv {
    display: flex;
    padding: 15px;
    border-bottom: 1px solid #EBEBEB;
    div:nth-child(1) {
      flex: 0 0 40px;
      height: 40px;
      border-radius: 50%;
      image {
        width: 100%;
        height: 100%;
        border-radius: 50%;

      }
    }
    div:nth-child(2) {
      flex: 1;
      font-size: 12px;
      display: flex;      
      flex-direction: column;
      justify-content: center;
      padding-left: 15px;
      span:nth-child(2){
        padding-top: 10px;
        color: #666666;
      }
      .position {
        color: #999999;
        font-size: 12px;
      }
      .name {
        font-size: 15px;
        color: #333333;
      }
    }
    div:nth-child(3) {
      font-size: 12px;
      display: flex;      
      flex-direction: column;
      justify-content: center;
      image {
        width: 13px;
        height: 20px;
        margin: 0 auto;
      }
      span{
        padding-top: 8px;
        color: #FFAA33;
        font-size: 14px;
      }
    }
  }
  .showmsg {
    font-size: 12px;
    padding: 15px;
    .time {
      background-color: #cccccc;
      width: 43px;
      height: 25px;
      line-height: 25px;
      text-align: center;
      border-radius: 10px;
      margin: 0 auto;
      color: #ffffff;
    }
    .sessionMsg {
      display: flex;   
      justify-content: flex-end;
      padding-top: 10px;
      .msgp {
        position: relative;
        display: flex;
        flex-direction: column;
        flex: 0.8;
        box-shadow: 0px 0px 10px rgba(0,0,0,0.1) ;
        border-radius: 5px;
        image {
          width: 30px;
          height: 30px;
          position: absolute;
          left: 10px;
          top: 50%;
          margin-top: -15px;
        }        
        p {          
          position: relative;
          height: 60px;
          line-height: 60px;
          background-color: #ffffff;
          font-size: 15px;
          padding-left: 50px;
          color: RGBA(179, 179, 179, 1);
          border-bottom: 1px solid RGBA(238, 238, 238, 1);
        }        
        .wait {
          height: 40px;
          line-height: 40px;
          color: RGBA(255, 75, 0, 1);
          text-align: center;
          font-size: 14px;
          padding-left: 0;
        }
      }
      .sendimg {
        position: relative;
        flex: 0 0 50px;
        div {          
          width: 40px;
          height: 40px;
          box-shadow:none;
          border-radius: 50%;
          bottom: 10px;
        }
        image {
          position: absolute;
          bottom: 0px;
          left: 7px;
          width: 100%;
          height: 100%;
          border-radius: 50%;         
          width: 40px;
          height: 40px;
        }
      }
    }
    .isagree {
      padding: 30px 0;
      text-align: center;
      span {
        padding: 5px 13px;
        background-color: RGBA(204, 204, 204, 1);
        color: #ffffff;
        border-radius: 10px;
        font-size: 14px;
      }
    }
    .recevidebg {      
      box-shadow: 0px 0px 10px rgba(0,0,0,0.1) ;
      padding: 20px;
      padding-top: 20px;
      border-radius: 5px;
    }
    .recevide {
      display: flex;   
      border-bottom: 1px solid RGBA(238, 238, 238, 1);   
      padding-bottom: 10px;
      .recevidemsg {
        flex: 1;
        p{
          color: RGBA(153, 153, 153, 1);
          padding-top: 10px;
          font-size: 14px;
          image {
            width: 8px;
            height: 12px;
            margin-right: 10px;
          }
        }
        p:nth-child(1) {
          color: RGBA(51, 51, 51, 1);
          font-size: 17px;
          padding-top: 0;
        }
      }
      .recevideimg {
        flex: 0 0 80px;
        div {          
          width: 60px;
          height: 60px;
          margin: 0 auto;
        }
        image {
          width: 60px;
          height: 60px;
          border-radius: 50%;
        }
      }
    }
    .recevideTip {
      color: RGBA(51, 51, 51, 1);
      padding-top: 15px;
      font-size: 14px;
    }
    .changePhone {
      padding: 20px;
      text-align: center;
      span {
        background-color: RGBA(204, 204, 204, 1);
        color: #ffffff;
        font-size: 14px;
        padding: 5px 15px;
        border-radius: 15px;
      }
    }
  }
}
  
</style>

