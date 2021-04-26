<!--
 * @Author: your name
 * @Date: 2021-04-26 14:42:51
 * @LastEditTime: 2021-04-26 17:38:09
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\add_address.vue
-->
<template>
  <view class="address_page">
    <view class="item">
      <text class="title">联系人</text>
      <input class="input" placeholder="收货人姓名" />
    </view>
    <view class="item">
      <text class="title">手机号</text>
      <input class="input" placeholder="收货人手机号" />
    </view>
    <view class="item" @click="show = true">
      <text class="title">选择地址</text>
      <u-picker v-model="show" mode="region" @confirm="confirm"></u-picker>
        <view class="input">{{province}},{{city}},{{area}}</view>
    </view>

    <view class="item">
      <text class="title">详细地址</text>
      <input class="input" placeholder="请输入详细地址" />
    </view>
    <view class="item">
      <text class="title">设为默认</text>
      <switch class="choose" color="#fa436a" :checked="true" />
    </view>
    <button class="sub_btn">提交</button>
  </view>
</template>

<script>
export default {
  data() {
    return {
      show: false,
       province:"北京市",
       city:"市辖区",
        area:"东城区"
    };
  },
  methods: {
    confirm(e) {
      console.log(e);
       this.province=e.province.label;
       this.city=e.city.label;
       this.area=e.area.label;
    },
  },
  
};
function clickFn() {
      show=!show;
  }
</script>

<style lang="scss" scoped>
page {
  background: #f8f8f8;
}
.address_page {
  padding-top: 20rpx;
  .item {
    display: flex;
    position: relative;
    align-items: center;
    position: relative;
    padding: 0 30rpx;
    height: 110rpx;
    background: #fff;
    border-bottom: 1rpx solid #f5f5f5;
    .title {
      font-size: 30rpx;
      color: #303133;
      width: 140rpx;
    }
    .input {
      font-size: 30rpx;
      color: #303133;
    }
  }
  .choose {
    position: absolute;
    right: 0;
    transform: scale(0.7);
  }
  .sub_btn {
    background: #fa436a;
    color: #fff;
    height: 80rpx;
    line-height: 80rpx;
    font-size: 34rpx;
    width: 690rpx;
    margin: 60rpx auto;
    border-radius: 10rpx;
    align-items: center;
    text-align: center;
  }
}
</style>