<template>
  <view class="content">
    <image class="logo" src="/static/logo.png"></image>
    <view class="text-area">
      <text class="title">{{title}}</text>
    </view>
    <button @click="callCloudFunctions">调用云函数</button>
  </view>
</template>

<script>
  export default {
    data() {
      return {
        title: 'Hello'
      }
    },
    onLoad() {

    },
    methods: {
      callCloudFunctions() {
        uniCloud.callFunction({
          name: 'login',
          data: {
            name: 'liming',
            age: 23
          },
          success(res) {
            console.log(res);
          }
        })
      }
    }
  }
</script>

<style lang="scss">
  .content {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    .logo {
      height: 200rpx;
      width: 200rpx;
      margin-top: 200rpx;
      margin-left: auto;
      margin-right: auto;
      margin-bottom: 50rpx;
    }

    .text-area {
      display: flex;
      justify-content: center;

      .title {
        font-size: 36rpx;
        color: #8f8f94;
      }
    }
  }
</style>
