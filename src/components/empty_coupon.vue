<!--
 * @Author: your name
 * @Date: 2021-04-23 15:12:34
 * @LastEditTime: 2021-04-23 15:24:20
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\components\empty_coupon.vue
-->
<template name="empty_coupon">
  <view class="empty">
    <view class="empty_content">
      <text class="icon iconfont">&#xe622;</text>
      <text>暂无优惠券</text>
    </view>
    <view class="recommend">
      <view class="recommend_content">
        <view class="line"></view>
        <text class="name">为您推荐</text>
        <view class="line"></view>
      </view>
    </view>
    <product_list></product_list>
  </view>
</template>
<script>
import product_list from './product_list.vue';
export default {
  components: { product_list },};
</script>
<style lang="scss" scoped>
.empty {
  background: #fff;
  height: 100%;
  .empty_content {
    width: 100%;
    height: 420rpx;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 20rpx 0 80rpx;
    font-size: 28rpx;
    .iconfont {
      color: #fa436a;
      font-size: 200rpx;
      margin: 30rpx auto;
    }
  }
  .recommend {
    .recommend_content {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 40rpx 20% 20rpx;

      .line {
        border-bottom: 1rpx solid rgba(0, 0, 0, 0.15);
        width: 120rpx;
      }
      .name {
        margin: 0 10rpx;
        font-size: 28rpx;
      }
    }
  }
}
</style>