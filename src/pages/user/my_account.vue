<!--
 * @Author: your name
 * @Date: 2021-04-19 10:57:11
 * @LastEditTime: 2021-04-25 17:52:35
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\my_account.vue
-->
<template>
  <view class="my_account_page">
    <view class="summary">
      <view class="total_assets_row">
        <view class="total_assets">
          <view class="assets">总资产(元)</view>
          <view class="money">0.00</view>
        </view>
      </view>
      <view class="cumulative_row">
        <view class="cumulative_recharge">
          <view>累计充值(元)</view>
          <view class="money">0.00</view>
        </view>
        <view class="cumulative_recharge">
          <view>累计消费(元)</view>
          <view class="money">0.00</view>
        </view>
      </view>
    </view>
    <view class="nav">
      <view class="item">
        <text class="icon iconfont">&#xe60d;</text>
        <text>账单记录</text>
      </view>
      <view class="item">
        <text class="icon iconfont">&#xe621;</text>
        <text>充值记录</text>
      </view>
      <view class="item">
        <text class="icon iconfont">&#xe6a1;</text>
        <text>消费记录</text>
      </view>
      <navigator class="item" url="/pages/more_pages/points_details">
        <text class="icon iconfont">&#xe755;</text>
        <text>积分中心</text>
      </navigator>
    </view>
    <navigator class="get_coupons" url="/pages/user/serve/voucher_center">
      <view class="item">
        <view class="content_right">
          <view class="get_coupons_name">领取优惠券</view>
          <text>满减享优惠</text>
        </view>
        <text class="icon iconfont">&#xe655;</text>
      </view>
    </navigator>
  </view>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
.my_account_page {
  background-color: #fff;
  height: 100vh;
  padding: 32rpx 20rpx;
  .summary {
    position: relative;
    background-color: #fa436a;
    color: #d8d1d1;
    padding: 30rpx;
    height: 320rpx;
    opacity: 0.9;
    border-radius: 20rpx;
    font-size: 30rpx;
    .total_assets_row {
      display: flex;
      position: absolute;
      justify-content: space-between;
    }
    .money {
      color: #fff;
      font-size: 38rpx;
      margin: 5rpx;
    }
    .cumulative_row {
      position: absolute;
      bottom: 20rpx;
      display: flex;
      justify-content: space-between;
      width: 500rpx;
    }
  }
  .nav {
    display: flex;
    border-bottom: 1px solid #f5f5f5;
    .item {
      flex: 1;
      display: inline-block;
      margin: 20rpx;
      text-align: center;
      color: #999;
      font-size: 28rpx;
      .iconfont {
        color: #fa436a;
        font-size: 50rpx;
        display: block;
        //   margin: 0 auto;
        margin-bottom: 10rpx;
      }
    }
  }
  .get_coupons {
    display: flex;
    color: #fa436a;
    .item {
      display: flex;
      width: 100%;
      background-color: #fff3f3;
      justify-content: space-between;
      border-radius: 24rpx;
      padding: 10rpx 0;
      margin: 20rpx 10rpx;
      .content_right {
        margin-left: 20rpx;
        .get_coupons_name {
          font-weight: bold;
          height: 40rpx;
          font-size: 28rpx;
        }
        text {
          font-size: 22rpx;
        }
      }
      .iconfont {
        font-size: 40rpx !important;
        margin-right: 20rpx;
        line-height: 2.5;
      }
    }
  }
}
</style>