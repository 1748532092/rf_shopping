<!--
 * @Author: your name
 * @Date: 2021-04-20 16:57:44
 * @LastEditTime: 2021-04-20 17:39:51
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\serve\notice.vue
-->
<template>
  <view>
    <view class="notice_item" v-for="(item,index) in 4" :key="index">
      <text class="time">2021-04-12 16:29</text>
      <view class="content">
        <text class="title">第三个十多个梵蒂冈</text>
        <view class="picture">
          <image class="pic" src="../../../static/vip-card-bg.png"></image>
        </view>
        <text class="introduce"
          >第三个十多个梵蒂冈第三个十多个梵蒂冈第三个十多个梵蒂冈第三个十多个梵蒂冈第三个十多个梵蒂冈</text
        >
        <view class="detail_btn">
          <text>查看详情</text>
          <view class="icon iconfont">&#xe62e;</view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.notice_item {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #f8f8f8;
  .time {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 80rpx;
    padding-top: 10rpx;
    font-size: 26rpx;
    color: #7d7d7d;
  }
  .content {
    width: 710rpx;
    padding: 0 24rpx;
    background-color: #fff;
    border-radius: 4rpx;
    font-size: 28rpx;
     
    .title {
      display: flex;
      align-items: center;
      height: 90rpx;
      font-size: 32rpx;
      color: #303133;
    }
    .picture {
      width: 100%;
      height: 260rpx;
      position: relative;
      .pic {
        display: block;
        width: 100%;
        height: 100%;
        border-radius: 6rpx;
      }
    }
    .introduce {
      display: inline-block;
      padding: 16rpx 0;
      font-size: 28rpx;
      color: #606266;
      line-height: 38rpx;
      border-bottom: 1px solid #e4e7ed;
    }
    .detail_btn {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 80rpx;
      color: #707070;
      position: relative;
      font-size: 28rpx;
      .iconfont {
        position: absolute;
        right: 0;
      }
    }
  }
}
</style>