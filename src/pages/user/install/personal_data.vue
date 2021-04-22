
<template>
  <view class="user_information">
    <view class="user_profile">
      <image class="photo_img" src="../../../static/missing-face.png"></image>
    </view>
    <view class="input_module">
      <view class="input_item">
        <text class="input_title">手机号</text>
        <input class="input_content" placeholder="请输入手机号码" />
      </view>
      <view class="input_item">
        <text class="input_title">昵 称</text>
        <input class="input_content" placeholder="请输入您的昵称" />
      </view>
      <view class="input_item">
        <text class="input_title">姓 名</text>
        <input class="input_content" placeholder="请输入您的姓名" />
      </view>
      <view class="input_item">
        <text class="input_title">性 别</text>
        <radio-group>
          <label class="options">
            <radio color="#fa436a"></radio>
            <text class="options_content">未知</text>
          </label>
           <label class="options">
            <radio color="#fa436a"></radio>
            <text class="options_content">男</text>
          </label>
           <label class="options">
            <radio color="#fa436a"></radio>
            <text class="options_content">女</text>
          </label>
        </radio-group>
      </view>
      <view class="input_item">
        <text class="input_title">生 日</text>
        <picker mode="date" v-model="date" @change="bindDateChange">
          <view class="date" style="background: none">{{
            date || "请选择日期"
          }}</view>
        </picker>
      </view>
      <view class="input_item">
        <text class="input_title">Q Q</text>
        <input class="input_content" placeholder="请输入您的QQ" />
      </view>
      <view class="input_item">
        <text class="input_title">邮 箱</text>
        <input class="input_content" placeholder="请输入您的邮箱" />
      </view>
      <button class="modify_btn">修改资料</button>
    </view>
  </view>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.user_information {
  .user_profile {
    background: url("../../../static/user_bg.png");
    display: flex;
    align-items: center;
    justify-content: center;
    height: 320rpx;
    padding: 40rpx 30rpx 0;
    overflow: hidden;
    position: relative;
    .photo_img {
      display: inline-block;
      width: 200rpx;
      height: 200rpx;
      border: 5rpx solid #fff;
      border-radius: 50%;
    }
  }
  .input_module {
    padding: 40rpx 60rpx;
    background: #f8f6fc;
    .input_item {
      display: flex;
      padding: 0 30rpx;
      background: #fff;
      height: 80rpx;
      border-radius: 4px;
      margin-bottom: 30rpx;
      height: 80rpx;
      line-height: 80rpx;
      .date {
        height: 80upx;
        line-height: 80upx;
        font-size: 30rpx;
        color: black;
      }
      .input_title {
        width: 100rpx;
        font-size: 26rpx;
        color: #606266;
        white-space: pre;
      }
      radio-group {
        display: inline-block;
     .options {
          margin-right: 20rpx;
          position: relative;
          .iconfont {
          }
          .options_content {
            
            font-size: 28rpx;
            color: #606266;
          }
        }
      }
      .input_content {
        width: calc(100% - 100rpx);
        height: 80rpx;
        line-height: 80rpx;
        font-size: 30rpx;
        color: #303133;
        font-size: 28rpx;
      }
    }
    .modify_btn {
      background-color: #fa436a;
      color: #ffffff;
      width: 620rpx;
      height: 80rpx;
      line-height: 80rpx;
      font-size: 34rpx;
      border-radius: 2em;
      margin-top: 70rpx;
    }
  }
}
</style>