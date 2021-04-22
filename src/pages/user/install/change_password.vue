<template>
  <view>
    <view class="chang_password">
      <view class="login_top">
        <text class="icon iconfont">&#xe628;</text>
        <view class="describe">
          <view class="title">Hi~</view>
          <text>修改密码 ！</text>
        </view>
        <image class="login-pic" src="../../../static/login-pic.png"></image>
      </view>
      <view class="login_content">
        <image class="login_content_bg" src="../../../static/login-bg.png"></image>
        <view class="main_content">
          <view class="login_form">
            <view class="input_item">
              <text class="icon iconfont">&#xe7aa;</text>
              <input class="input_text" placeholder="请输入手机号码" />
            </view>
            <view class="input_item">
              <text class="icon iconfont">&#xe6c3;</text>
              <view class="input_content">
                <view>
                  <input class="input_text" placeholder="请输入验证码" />
                </view>
                <button class="get_verification_code">获取验证码</button>
              </view>
            </view>
            <view class="input_item">
              <text class="icon iconfont">&#xe682;</text>
              <input class="input_text" placeholder="请输入密码" />
            </view>
             <view class="input_item">
              <text class="icon iconfont">&#xe682;</text>
              <input class="input_text" placeholder="请输入确认密码" />
            </view>
          </view>
           <view class="login_tips">
            <text>马上登陆</text>
            <text>返回主页</text>
          </view>
          <button class="login_btn">修改密码</button>
        </view>
        <view class="login_bottom">RF商城 版权所有</view>
      </view>
    </view>
  </view>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.chang_password {
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
      height: 120vw;
      margin: 0 3vw;
    }
    .main_content {
      width: 94vw;
      position: absolute;
      top: 0;
      left: 3vw;
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
            font-size: 50rpx;
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
          .input_content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            .get_verification_code {
              width: 200rpx;
              height: 80rpx;
              background-color: #fff;
              display: flex;
              justify-content: center;
              align-items: center;
              border-radius: 12rpx;
              font-size: 28rpx;
              color: #606266;
              line-height: 80rpx;
              padding: 15rpx 0;
            }
          }
        }
      }
      .login_tips {
        display: flex;
        justify-content: space-between;
        padding: 0 50rpx;
        font-size: 28rpx;
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