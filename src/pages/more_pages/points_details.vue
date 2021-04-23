<!--
 * @Author: your name
 * @Date: 2021-04-23 08:54:03
 * @LastEditTime: 2021-04-23 15:08:57
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\points_details.vue
-->
<template>
  <view class="points_details">
    <view class="header">
      <view class="title">当前积分</view>
      <text class="current_num">0</text>
      <view class="line"></view>
      <view class="navigation">
        <view class="item">
          <text class="points">0</text>
          <text class="title">累计积分</text>
        </view>
        <view class="item">
          <text class="points">0</text>
          <text class="title">累计消费</text>
        </view>
        <view class="item">
          <text class="points">0</text>
          <text class="title">冻结积分</text>
        </view>
      </view>
      <view class="tab">
        <view class="item active">分值明细</view>
        <!-- <score_details ></score_details> -->
         <view class="item">分值提升</view>
         <!-- <score_increase></score_increase> -->
      </view>
    </view>
  </view>
</template>
<script>
import score_details  from "../../components/score_details"
import score_increase  from "../../components/score_increase"
export default {
    components:{
        score_details,
        score_increase,
    }
};
</script>

<style lang="scss" scoped>
.points_details {
  .header {
    width: 100%;
    height: 420rpx;
    background: #fa436a;
    color: white;
    padding: 20rpx 0;
    text-align: center;
    position: relative;
    font-size: 28rpx;
    .title {
    }
    .current_num {
      margin-top: 10rpx;
      font-size: 50rpx;
    }
    .line {
      width: 10%;
      height: 3rpx;
      background-color: #fff;
      margin: 20rpx auto 30rpx;
    }
    .navigation {
      display: flex;
      width: 100%;
      .item {
        flex: 1;
        display: flex;
        flex-direction: column;
        .points {
          font-size: 34rpx;
        }
        .title {
        }
      }
    }
    .tab {
      position: absolute;
      bottom: -2rpx;
      display: flex;
      width: 80%;
      margin: 0 10%;
      border-radius: 20rpx 20rpx 0 0;
      background-color: #f7f7f7;
      height: 80rpx;
      .item{
          flex: 1;
          text-align: center;
          line-height: 80rpx;
          color: #fa436a;
      }
      .active{
          color:#bbb;
      }
    }
  }
}
</style>
