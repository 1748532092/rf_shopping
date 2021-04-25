<!--
 * @Author: your name
 * @Date: 2021-04-20 14:40:23
 * @LastEditTime: 2021-04-25 18:33:54
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\install\about.vue
-->
<template>
  <view class="about">
    <navigator class="item" v-for="(item, index) in list" :key="index" :url="item.url">
      <text class="item_title">{{ item.name }}</text>
      <text class="icon iconfont">&#xe62e;</text>
    </navigator>
    <view class="share">
      <view class="share_link">
        <view class="icon iconfont">&#xe658;</view>
        <text>分享商城二维码给好友</text>
      </view>
      <view class="qrcode">
        <view class="qrcode_img">
          <!-- 获取二维码的方法 -->
          <view class="img_size"></view>
        </view>
        <text class="qrcode_title">商城二维码</text>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          id: "1",
          name: "商城介绍",
          url: "/pages/user/about_shop/about_shop"
        },
        {
          id: "2",
          name: "注册协议",
          url: "/pages/user/about_shop/reg_agreement"
        },
        {
          id: "3",
          name: "充值协议",
           url: "/pages/user/about_shop/rec_agreement"
        },
        {
          id: "4",
          name: "隐私协议",
           url: "/pages/user/about_shop/pri_agreement"
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.about {
  background: #f8f8f8;
  padding: 20rpx 0;
  .item {
    display: flex;
    padding: 20rpx 30rpx;
    position: relative;
    justify-content: center;
    font-size: 30rpx;
    background: #fff;
    height: 50rpx;
    line-height: 50rpx;
    border-bottom: 1px solid #e4e7ed;
    .item_title {
      flex: 1;
      margin-right: 10rpx;
    }
  }
  .share {
    padding: 30rpx 0 0;
    margin-top: 20rpx;
    background: #fff;
    border-radius: 10rpx;
    .share_link {
      display: flex;
      align-items: center;
      color: #303133;
      font-size: 30rpx;
      margin-left: 30rpx;
      .iconfont {
        
        margin-right: 16rpx;
        font-size: 28rpx;
      }
    }
    .qrcode {
      padding: 30rpx 0;
      text-align: center;
      .qrcode_img {
        display: flex;
        justify-content: center;
        align-items: center;
        .img_size {
          width: 300rpx;
          height: 300rpx;
        }
      }
      .qrcode_title {
        font-size: 28rpx;
      }
    }
  }
}
</style>