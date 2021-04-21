<!--
 * @Author: your name
 * @Date: 2021-04-21 08:47:40
 * @LastEditTime: 2021-04-21 09:40:25
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\serve\address.vue
-->
<template>
  <view>
    <empty_address></empty_address>
    <view class="add_address">
      <button class="add_btn">新增收货地址</button>
    </view>
  </view>
</template>

<script>
import empty_address from "../../../components/empty_address";
export default {
  components: { empty_address },
};
</script>

<style lang="less" scoped>
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
  }
}
</style>