<template>
  <view class="logo_page">
    <view class="logo">
      <image class="logo_img" src="../../static/logo.png"></image>
    </view>
    <view style="text-align:center">
      <navigator class="existing_account" url="/pages/more_pages/existing_account" hover-class="none">已有账号登录</navigator>
      <navigator class="register" url="/pages/more_pages/register" hover-class="none">立即注册</navigator>
    </view>
    <view class="agreement">
      <text class="icon iconfont">&#xe60f;</text>
      <text class="content">登录表示同意</text>
      <text class="text">《RF商城协议》</text>
    </view>
    <view class="footer">
      <view class="liner"></view>
      <view class="title">
        <text>其他登录方式</text>
      </view>
      <view class="login_type">
        <button class="icon iconfont">&#xe68a;</button>
      </view>
    </view>
  </view>
</template>
<script >
</script>
<style lang="scss" scoped>
.logo_page {
  padding-top: 80rpx;
  .logo {
    text-align: center;
    margin-bottom: 80rpx;
    .logo_img {
      width: 180rpx;
      height: 180rpx;
      border-radius: 28rpx;
    }
  }

  .existing_account {
    width: 630rpx;
    border-radius: 100rpx;
    height: 80rpx;
    line-height: 80rpx;
    font-size: 34rpx;
    font-weight: normal;
    color: #fa436a;
    border: 1rpx solid #fa436a;
    background: #fff;
    margin: 0 auto;
  }
  .register {
    width: 630rpx;
    border-radius: 100rpx;
    height: 80rpx;
    line-height: 80rpx;
    font-size: 34rpx;
    font-weight: normal;
    color: #fa436a;
    border: 1rpx solid #fa436a;
    background: #fff;
     margin: 50rpx auto 0;
  }
  .agreement {
    display: flex;
    font-size: 28rpx;
    justify-content: center;
    align-items: center;
    margin-top: 50rpx;
    padding-bottom: 30%;
    .iconfont {
      font-size: 40rpx;
      color: #fa436a;
      align-items: center;
      padding: 6rpx;
    }
    .content {
      margin: 0 4rpx 0 10rpx;
    }
    .text {
      color: #fa436a;
    }
  }
  .footer {
    width: 400rpx;
    height: 44rpx;
    position: relative;
    margin: 100rpx auto;
    .liner {
      width: 100%;
      height: 1rpx;
      background-color: #ccc;
      position: relative;
      top: 50%;
    }
    .title {
      text-align: center;
      width: 180rpx;
      height: 44rpx;
      line-height: 44rpx;
      font-size: 28rpx;
      margin: 0 auto;
      color: #606266;
      background-color: #fff;
      position: relative;
    }
    .login_type {
      display: flex;
      width: 100%;
      align-items: center;
      justify-content: center;
      margin-top: 20rpx;
      button {
        position: relative;
        display: block;
        margin-left: auto;
        margin-right: auto;
        padding-left: 28rpx;
        padding-right: 28rpx;
        text-align: center;
        border-radius: 5px;
        color: rgb(45, 230, 106);
        background-color: #fff;
      }
    }
  }
}
</style>