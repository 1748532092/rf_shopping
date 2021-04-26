<!--
 * @Author: your name
 * @Date: 2021-04-21 08:47:40
 * @LastEditTime: 2021-04-26 18:24:42
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\serve\address.vue
-->
<template>
  <view class="pages">
    <!-- <empty_address></empty_address>  -->
    <view class="address_details">
      <view class="left">
        <text class="address">福建省 厦门市 集美区</text>
        <view class="information">
          <text class="name">小2</text>
          <text class="number">12345678901</text>
        </view>
      </view>
      <view class="right">
        <text class="icon iconfont">&#xe630;</text>
      </view>
    </view>
    <text class="tips">提示：长按可删除当前收货地址。最多只能存在一个默认地址。</text>
    <view class="no_more">没有更多了</view>
    <view class="add_address">
      <navigator class="add_btn" url="/pages/more_pages/add_address"
        >新增收货地址</navigator
      >
    </view>
  </view>
</template>

<script>
import empty_address from "../../../components/empty_address";
export default {
  components: { empty_address },
};
</script>

<style lang="scss" scoped>
.pages {
  background: #f8f8f8;
  height: 100%;
  padding-top: 10rpx;
}
.address_details {
  align-items: center;
  display: flex;
  margin: 20rpx;
  padding: 20rpx 30rpx;
  background: #fff;
  position: relative;
  .left {
    .address {
      font-size: 28rpx;
    }
    .information {
      font-size: 26rpx;
      color: #cccaca;
      margin-top: 20rpx;
      .name {
        margin-right: 20rpx;
      }
    }
  }
  .right {
    position: absolute;
    right: 30rpx;
    .iconfont {
    }
  }
}
.tips{
  font-size: 24rpx;
  color:red;
  margin-left: 30rpx;
}
.no_more{
  margin-top: 20rpx;
  text-align: center;
  color: #6e6363;
  font-size: 26rpx;
}
.add_address {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 120rpx;
  background: #f8f8f8;
  .add_btn {
    background: #fa436a;
    color: #fff;
    margin: 20rpx 30rpx;
    border-radius: 2em;
    font-size: 28rpx;
    height: 80rpx;
    line-height: 80rpx;
    text-align: center;
  }
}
</style>