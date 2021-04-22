<!--
 * @Author: your name
 * @Date: 2021-04-15 14:23:42
 * @LastEditTime: 2021-04-22 15:49:57
 * @LastEditors: your name
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\components\electric.vue
-->
<template name="electricTab">
  <view class="empty">
    <view class="empty_content">
      <view class="icon iconfont">&#xe60e;</view>
      <view class="empty_text">暂无该分类产品~</view>
    </view>
    <view class="empty_recommend">
      <view class="liner"></view>
      <view class="recommend_text">
        <span>为您推荐</span>
      </view>
    </view>
  </view>
</template>

<script>
export default {};
</script>
    <style lang="scss" scoped>
.empty_content {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #fff;
  margin-top: 100rpx;
  .iconfont {
    font-size: 200rpx;
    color: red;
  }
  .empty_text {
    margin-top: 40rpx;
    font-size: 28rpx;
    color: rgb(80, 75, 75);
  }
}
.empty_recommend {
  width: 400rpx;
  height: 22px;
  position: relative;
  margin: 100rpx auto;
}
.liner {
  width: 100%;
  height: 1rpx;
  background-color: #ccc;
  position: relative;
  top: 50%;
}
.recommend_text {
  text-align: center;
  width: 60px;
  height: 22px;
  line-height: 22px;
  font-size: 28rpx;
  margin: 0 auto;
  color: rgb(80, 75, 75);
  background-color: #fff;
  position: relative;
  z-index: 3;
}
</style>