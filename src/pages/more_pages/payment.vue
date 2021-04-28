<template>
  <view class="pay_page">
    <view class="header">
      <!-- 状态栏占位 -->
      <view :style="{ paddingTop: statusBarHeight + 'px' }"></view>
      <view class="title">
        <text class="icon iconfont">&#xe61b;</text>
        <text class="tit">支付</text>
      </view>
      <view class="payment">
        <text class="pay_tit">支付金额</text>
        <view class="pay_money">¥100.00</view>
      </view>
    </view>
    <view class="pay_type_list">
      <view class="type_item">
        <text class="icon iconfont">&#xe61a;</text>
        <view class="content">
          <text class="tit">微信支付</text>
          <text>推荐使用微信支付</text>
        </view>
        <label class="radio">
          <radio></radio>
        </label>
      </view>
      <view class="type_item">
        <text class="icon iconfont">&#xe61a;</text>
        <view class="content">
          <text class="tit">预存款支付</text>
          <text>可用余额 ¥0.00</text>
        </view>
        <label class="radio">
          <radio></radio>
        </label>
      </view>
    </view>
    <button class="pay_btn">确认支付</button>
  </view>
</template>

<script>
export default {
  data() {
    return {
      statusBarHeight: 0,
    };
  },
  //第一次加载时调用
  created() {
    //获取手机状态栏高度
    this.statusBarHeight = uni.getSystemInfoSync()["statusBarHeight"];
  },
};
</script>

<style lang="scss" scoped>
.pay_page {
  font-size: 28rpx;
  background: #fff;
  height: 100%;
  .header {
    background: #fa436a;
    color: #ffffff;
    width: 100vw;
    height: 60vw;
    margin-bottom: 30rpx;
    .title {
      display: flex;
      padding-top: 25rpx;
      .iconfont {
        font-size: 40rpx;
      }
      .tit {
        font-size: 34rpx;
        margin-left: 40%;
      }
    }
    .payment {
      text-align: center;
      align-items: center;
      margin-top: 90rpx;
      .pay_tit {
        font-size: 32rpx;
        margin-bottom: 20rpx;
      }
      .pay_money {
        font-size: 74rpx;
      }
    }
  }
  .pay_type_list {
    margin: 60rpx 0;
    background-color: #fff;
    padding: 0 40rpx;
    .type_item {
      display: flex;
      padding: 0 30rpx;
      height: 80rpx;
      border: 2rpx solid rgba(0, 0, 0, 0.12);
      border-radius: 100rpx;
      margin-bottom: 30rpx;
      justify-content: space-between;
      align-items: center;
      .iconfont {
        color: #909399;
        font-size: 45rpx;
      }
      .content {
        flex: 1;
        color: #909399;
        .tit {
          margin-right: 20rpx;
        }
      }
      .radio {
        width: 50rpx;
        height: 50rpx;
      }
    }
  }
  .pay_btn {
    width: 70%;
    text-align: center;
    color: #fff;
    background: #fa436a;
    height: 80rpx;
    line-height: 80rpx;
    font-size: 34rpx;
    border-radius: 50px;
    margin-top: 70rpx;
  }
}
</style>