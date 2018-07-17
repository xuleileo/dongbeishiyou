<template>
  <div class="bg">
    <img class="banner" src="../../../static/assets/banner1.jpeg" alt=""  @click="toJianjie">
    <button class="button_map" @click="toMap">校园地图</button>
    <button class="button_share" @click="btn_share" open-type="share">炫耀大学给好友</button>

  </div>
</template>

<script>

export default {

  data () {
    return {
    
    }
  },
   methods: {
    toMap(){
      const url = '../home_map/main';
      wx.navigateTo({ url })
    },
    toJianjie(){
      const url = '../home_jianjie/main';
      wx.navigateTo({ url })
    }
   },

  created () {

  },
  onShareAppMessage: function (res) {
    if (res.from === 'button') {
      // 来自页面内转发按钮
      console.log(res.target)
    }
    return {
      title: '我在东北石油大学，我骄傲',
      path: '/pages/home/main'
    }
  }
}
</script>

<style>
.bg{
  text-align: center;
}
.banner{
  width: 100vw;
}
.button_map{
  width: 60vw;
  margin-left: 20vw;
  margin-top: 5vh;
  height: 45px;
  color: #333;
  background: #fff;
}
.button_share{
  width: 60vw;
  margin-left: 20vw;
  margin-top: 5vh;
  height: 45px;
  color: #fff;
  background: #62b900;
}
</style>
