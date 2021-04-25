<!--
 * @Author: your name
 * @Date: 2021-04-23 10:23:49
 * @LastEditTime: 2021-04-23 14:44:18
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\components\score_details.vue
-->
<template name="score_increase">
  <view>
    <view class="tips_box">
      <text class="name">购买商品可获得积分奖励</text>
      <navigator class="content" url="/pages/classification/classification" open-type="switchTab" hover-class="none"> 赚积分 </navigator>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.tips_box {
  width: 600rpx;
  height: 120rpx;
  margin: 20rpx 5%;
  position: relative;
  border-radius: 20rpx;
  background: #fff5e2;
  border: 1px solid #ffeac1;
  color: #c8a86b;
  text-align: center;
  display: flex;
  padding: 0 20rpx;
  .name {
    flex: 1;
    font-size: 24rpx;
    font-weight: bold;
    color: #c8a86b;
    margin: 0 20rpx;
    line-height: 120rpx;
    text-align: left;
  }
  .content {
    color: #c8a86b;
    border: 2rpx solid #c8a86b;
    text-align: center;
    height: 48rpx;
    margin: 36rpx 20rpx;
    width: 120rpx;
    border-radius: 10rpx;
    font-size: 24rpx;
    line-height: 2;
  }
}
</style>