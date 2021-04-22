<template>
  <view class="voucher_center">
    <view class="coupons_list">
      <view class="item">
        <view class="coupons_content">
          <view class="coupons_head">
            <view>
              <text class="coupons_icon">限</text>
              <text class="coupons_title">满减福利</text>
            </view>
            <view>
              <text class="coupons_value">¥ 1.00</text>
            </view>
          </view>
          <view class="coupons_center">
            <text>2020-12-09 17:17 ~ 2020-12-18 10:00</text>
            <text>满1.00可用</text>
          </view>
          <view class="coupons_explain">
            <text>部分产品使用</text>
            <text>每人限领1 已领29 剩余18%</text>
          </view>
        </view>
      </view>
      <view class="item">
        <view class="coupons_content op">
          <view class="coupons_head">
            <view>
              <text class="coupons_icon">全</text>
              <text class="coupons_title">优惠券</text>
            </view>
            <view>
              <text class="coupons_value">¥ 10.00</text>
            </view>
          </view>
          <view class="coupons_center">
            <text>2020-12-03 13：12 ~ 2020-12-25 14：50</text>
            <text>满100.00可用</text>
          </view>
          <view class="coupons_explain">
            <text>全场产品使用</text>
            <text>不限 已领120</text>
          </view>
        </view>
      </view>
      <view class="item">
        <view class="coupons_content">
          <view class="coupons_head">
            <view>
              <text class="coupons_icon">限</text>
              <text class="coupons_title">优惠</text>
            </view>
            <view>
              <text class="coupons_value">¥ 0.00</text>
            </view>
          </view>
          <view class="coupons_center">
            <text>2020-12-03 13：11 ~ 2020-12-03 13:11</text>
            <text>满0.00可用</text>
          </view>
          <view class="coupons_explain">
            <text>部分产品使用</text>
            <text>不限 已领0 剩余100%</text>
          </view>
        </view>
      </view>
      <view class="item">
        <view class="coupons_content op">
          <view class="coupons_head">
            <view>
              <text class="coupons_icon">限</text>
              <text class="coupons_title">优惠</text>
            </view>
            <view>
              <text class="coupons_value">¥ 0.00</text>
            </view>
          </view>
          <view class="coupons_center">
            <text>2020-12-03 13：11 ~ 2020-12-03 13:11</text>
            <text>满0.00可用</text>
          </view>
          <view class="coupons_explain">
            <text>部分产品使用</text>
            <text>不限 已领0</text>
          </view>
        </view>
      </view>
      <view class="item">
        <view class="coupons_content op">
          <view class="coupons_head">
            <view>
              <text class="coupons_icon">限</text>
              <text class="coupons_title">优惠</text>
            </view>
            <view>
              <text class="coupons_value">¥ 0.00</text>
            </view>
          </view>
          <view class="coupons_center">
            <text>2020-12-03 13：11 ~ 2020-12-03 13:11</text>
            <text>满0.00可用</text>
          </view>
          <view class="coupons_explain">
            <text>部分产品使用</text>
            <text>不限 已领0</text>
          </view>
        </view>
      </view>
      <view class="item">
        <view class="coupons_content">
          <view class="coupons_head">
            <view>
              <text class="coupons_icon">限</text>
              <text class="coupons_title">测试满减</text>
            </view>
            <view>
              <text class="coupons_value">¥ 100.00</text>
            </view>
          </view>
          <view class="coupons_center">
            <text>2020-12-03 13：11 ~ 2020-12-03 13:11</text>
            <text>满200.00可用</text>
          </view>
          <view class="coupons_explain">
            <text>部分产品使用</text>
            <text>每人限领2 已领43 剩余62%</text>
          </view>
        </view>
      </view>
      <view class="end">没有更多了~</view>
    </view>
  </view>
</template>
<script>
</script>
<style lang="scss" scoped>
.voucher_center {
  background-color: #f1f1f1;
  font-size: 28rpx;
  color: #333;
  .coupons_list {
    padding-top: 10rpx;
    .item {
      width: 92%;
      margin: 20rpx auto 10rpx;
      align-items: center;
      .coupons_content {
        border-radius: 12rpx;
        background-color: #fff;
        padding: 20rpx 30rpx;
      }
      .op {
        opacity: 0.4;
      }
      .coupons_head {
        display: flex;
        justify-content: space-between;
        .coupons_icon {
          background-color: #fa436a;
          color: #fff;
          display: inline-block;
          height: 32rpx;
          margin-top: 15rpx;
          width: 32rpx;
          font-size: 22rpx;
          text-align: center;
          line-height: 32rpx;
          border-radius: 4rpx;
          margin-right: 12rpx;
        }
        .coupons_title {
          font-size: 32rpx;
          color: #303133;
        }
        .coupons_value {
          font-size: 44rpx;
          color: #fa436a;
        }
      }
      .coupons_center {
        display: flex;
        justify-content: space-between;
        color: #909399;
        font-size: 24rpx;
        padding: 10rpx 0;
        margin-bottom: 10rpx;
        border-bottom: 1rpx solid rgba(0, 0, 0, 0.05);
      }
      .coupons_explain {
        display: flex;
        justify-content: space-between;
        padding: 10rpx;
        color: #909399;
      }
    }
    .end {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 80rpx;
      color: #909399;
    }
  }
}
</style>