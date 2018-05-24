<template lang="pug">
#init
  .bg
    img(src="/static/qidongye.png")
    .inre 朋友，从心意开始！
</template>
<style lang="less">
@import url("~@/styles/index.less");
  #init {
    height: 100vh;display: flex;color: @defaultColor;
    flex-direction:column;
    justify-content: center;
    .bg{margin: auto;
      img{width: 50vw;height: 50vw;}
      .inre{text-align: center;line-height: 30px;padding-left: 15px;}
    }
  }
</style>
<script>
export default {
  onLoad () {
    this.$router.push({
      path: '/pages/SessionPage/SessionSuccess'
    })
  }
}
</script>


