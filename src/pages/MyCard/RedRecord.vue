<template lang="pug">
#RedRecord
  #tab
    span(@click="currentTab=0")
      div(:class="{hot:!currentTab}") 发放记录
    span(@click="currentTab=1")
      div(:class="{hot:currentTab}") 领取记录
  swiper.content(:current="currentTab" class="swiper-box" duration="300" @change="swiperChange")
    swiperItem
      .accumulate 累积发放:#[b.red ￥{{distribution}}] 累积领取:#[b.red ￥{{collection}}]
      scrollView.oneScroll(scroll-y @scrolltolower="toLow") 内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分内容部分结束
    swiperItem 领取记录
  canvas(canvas-id='myCanvas',style="width: 330px;height: 250px;background:#ccc")
  img(:src="fximg")
</template>
<script>
// import api from '@/utils/api'
import wxp from 'minapp-api-promise'
import wx from '@/utils/wx'
export default {
  data () {
    return {
      winWidth: 0,
      winHeight: 0,
      currentTab: 0,
      fximg: '',
      distribution: 0, // 累积发放
      collection: 0 // 累积领取
    }
  },
  onShareAppMessage: function (res) {
    console.log(typeof this.fximg)
    if (res.from === 'button') {
      // 来自页面内转发按钮
      console.log(res.target, this.fximg)
    }
    return {
      title: '自定义转发标题',
      path: '/pages/MyCard/SendCard?id=123',
      imageUrl: this.fximg
    }
  },
  methods: {
    toLow (e) {
      console.log('这里就是滚动到底部了')
      // wx.canvasToTempFilePath({
      //   x: 0,
      //   y: 0,
      //   width: 50,
      //   height: 50,
      //   destWidth: 100,
      //   destHeight: 100,
      //   canvasId: 'myCanvas',
      //   success: function (res) {
      //     console.log(res.tempFilePath)
      //   }
      // })
    },
    async ToTempFile () {
      await wxp.canvasToTempFilePath({
        x: 0,
        y: 0,
        width: 50,
        height: 50,
        destWidth: 100,
        destHeight: 100,
        canvasId: 'myCanvas'
      })
    },
    onHot () {
      console.log(888888)
    },
    swiperChange (e) {
      let { current } = e.target
      this.currentTab = current
    }
  },
  mounted () {
    const ctx = wxp.createCanvasContext('myCanvas')
    let that = this
    ctx.setFontSize(16)
    ctx.fillText('XX想认识你，并发了一个红包', 0, 20)
    ctx.drawImage('/static/qidongye.png', 0, 0, 150, 150)
    ctx.fillText('阮儿', 50, 100)
    ctx.fillText('广东省易上云有限公司', 50, 120)
    ctx.fillText('CEO', 50, 140)
    ctx.fillText('13751596693', 50, 160)
    ctx.draw(false, function () {
      wx.canvasToTempFilePath({
        // x: 0,
        // y: 0,
        canvasId: 'myCanvas',
        // fileType: 'jpg',
        // width: 200,
        // height: 300,
        // destWidth: 1400,
        // destHeight: 1400,
        // quality: 1,
        success: function (res) {
          that.fximg = res.tempFilePath
          console.log(res)
        }
      })
    })
    // wx.saveImageToPhotosAlbum({
    //   filePath: this.fximg,
    //   success (res) {
    //     console.log(res, '成功')
    //   }
    // })
    // wx.previewImage({
    //   urls: [that.fximg] // 需要预览的图片http链接列表
    // })
  },
  computed: {

  },
  async onLoad () {
    // 获取系统消息
    let info = await wxp.getSystemInfo()
    this.winWidth = info.windowWidth
    this.winHeight = info.windowHeight
    console.log(this.winHeight)
    let login = await wxp.login()
    console.log(login)
  }
}
</script>

<style lang="less" scoped>
@import url("~@/styles/index.less");
#RedRecord{
  background: @bodybg;display: flex; flex-direction: column;height: 100vh;color:#666;
  #tab{display: flex;font-size: 16px;line-height: 45px;background:@defaultBG;flex:45px 0;
    .hot{color: @primary-color;border-bottom: 3px solid @primary-color;}
    span{flex: 1;display: flex;justify-content:center;
      div{padding: 0 5px;}
    }
  }
  .content{ flex:1;
    .accumulate{display:flex;justify-content:center; font-size:12px;line-height:35px;color:#333;
      .red{color:@primary-color;}
    }
    .oneScroll{
      background:@defaultBG;border-radius:5px;padding-top:0px;height:90%;width: 90%;
      margin: auto;box-sizing: border-box; overflow: hidden;padding: 15px;
      
    }
  }
}
</style>
