<template>
  <view>
    <view class="existing_account_login">
      <view class="login_top">
        <text class="icon iconfont">&#xe62e;</text>
        <view class="describe">
          <view class="title">Hi~</view>
          <text>RF商城欢迎您</text>
        </view>
        <image class="login-pic" src="../../static/login-pic.png"></image>
      </view>
      <view class="login_content">
        <image class="login_content_bg" src="../../static/login-bg.png"></image>
        <view class="main_content">
          <view class="nav_bar">
            <view class="nav_bar_item">登录</view>
            <view class="nav_bar_item nav_bar_item_active">注册</view>
          </view>
          <view class="login_form">
            <view class="input_item">
              <text class="icon iconfont">&#xe709;</text>
              <input class="input_text" placeholder="请输入手机号码" />
            </view>
            <view class="input_item">
              <text class="icon iconfont">&#xe608;</text>
              <input class="input_text" placeholder="请输入密码" />
            </view>
          </view>
          <button class="login_btn">注册</button>
        </view>
        <view class="login_bottom">RF商城 版权所有</view>
      </view>
    </view>
  </view>
</template>
<script>
export default {};
</script>
<style lang="less" scoped>
.existing_account_login {
  width: 100%;
  position: relative;
  .login_top {
    height: 460rpx;
    position: relative;
    background-color: #fa436a;
    color: #ffffff;
    .iconfont {
      position: absolute;
      left: 40rpx;
      z-index: 9999;
      padding-top: 25px;
      top: 40rpx;
      font-size: 48rpx;
      color: #fff;
    }
    .describe {
      position: absolute;
      top: 200rpx;
      left: 40rpx;
      font-size: 48rpx;
    }
    .login-pic {
      position: absolute;
      width: 220rpx;
      height: 270rpx;
      right: 30rpx;
      top: 100rpx;
    }
  }
  .login_content {
    position: relative;
    top: -72rpx;
    .login_content_bg {
      width: 94vw;
      height: 94vw;
      margin: 0 3vw;
    }
    .main_content {
      width: 94vw;
      position: absolute;
      top: 0;
      left: 3vw;
      .nav_bar {
        display: flex;
        height: 100rpx;
        justify-content: center;
        align-items: center;
        position: relative;
        z-index: 10;
        .nav_bar_item {
          flex: 1;
          display: flex;
          height: 100%;
          font-size: 32rpx;
          line-height: 3.5;
          margin: 0 120rpx;
          justify-content: center;
        }
        .nav_bar_item_active {
          border-bottom: 5rpx solid;
          color: #fa436a;
        }
      }
      .login_form {
        width: 80%;
        margin: 50rpx auto;

        .input_item {
          position: relative;
          height: 90rpx;
          margin-bottom: 30rpx;
          .iconfont {
            position: absolute;
            left: 0;
            color: #fa436a;
            line-height: 90rpx;
          }
          .input_text {
            height: 90rpx;
            line-height: 90rpx;
            font-size: 30rpx;
            padding-left: 80rpx;
            border-bottom: 1rpx solid rgba(0, 0, 0, 0.1);
            text-overflow: clip;
            overflow: hidden;
            white-space: nowrap;
          }
        }
      }
      .login_btn {
        background-color: #fa436a;
        color: #ffffff;
        width: 630rpx;
        border-radius: 2em;
        margin-top: 70rpx;
        height: 80rpx;
        line-height: 80rpx;
        font-size: 34rpx;
      }
    }
    .login_bottom {
      width: 100%;
      margin-top: 80rpx;
      text-align: center;
      color: #fa436a;
      font-size: 32rpx;
    }
  }
}
</style>