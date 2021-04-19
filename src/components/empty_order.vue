
<template name="empty">
  <view class="empty">
    <view class="empty_content">
      <text class="icon iconfont">&#xe622;</text>
      <text>暂无订单</text>
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
<style lang="less" scoped>
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
      }
    }
  }
}
</style>