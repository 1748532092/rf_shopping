<!--
 * @Author: your name
 * @Date: 2021-04-12 15:45:00
 * @LastEditTime: 2021-04-23 16:11:51
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\user\user.vue
-->
<template>
  <view>
    <view class="user_top">
      <view class="user_info_box">
        <view class="user_info">
          <image class="photo_img" src="../../static/missing-face.png"></image>
          <navigator class="lod_text" url="/pages/more_pages/login" hover-class="none">登录/注册</navigator>
        </view>
      </view>
      <view class="vip_card_box">
        <view class="card_sign">普通用户</view>
        <view class="vip_title">
          <view class="icon iconfont">&#xe609;</view>
          <view class="vip_text">RF商城尊享会员</view>
        </view>
      </view>
    </view>
    <view class="user_content">
      <image class="arc" src="../../static/arc.png"></image>
      <view class="account_module">
          <navigator class="account_title" url="/pages/user/my_account" hover-class="none">
            <text class="icon iconfont">&#xe659;</text>
            <text class="title">我的账户</text>
            <view class="arrow_icon">
              <text class="icon iconfont">&#xe62e;</text>
            </view>
          </navigator>
        <view class="account_text">
          <navigator class="item" url="/pages/user/my_account" hover-class="none">
            <view class="data">0</view>
            <view class="name">余额</view>
          </navigator>
          <navigator class="item" url="/pages/user/my_coupon" hover-class="none">
            <view class="data">0</view>
            <view class="name">优惠券</view>
          </navigator>
          <navigator class="item" url="/pages/user/my_account" hover-class="none">
            <view class="data">0</view>
            <view class="name">积分</view>
          </navigator>
        </view>
      </view>
      <view class="account_module">
        <navigator class="account_title" url="/pages/user/my_order" hover-class="none">
          <text class="icon iconfont">&#xe60b;</text>
          <text class="title">全部订单</text>
          <view class="arrow_icon">
            <text class="icon iconfont">&#xe62e;</text>
          </view>
        </navigator>
        <view class="account_text">
          <navigator class="item" url="/pages/user/my_order?id=1" hover-class="none">
            <view class="icon iconfont">&#xe60d;</view>
            <view class="name">待付款</view>
          </navigator>
          <navigator class="item" url="/pages/user/my_order?id=2" hover-class="none">
            <view class="icon iconfont">&#xe60c;</view>
            <view class="name">待发货</view>
          </navigator>
          <navigator class="item" url="/pages/user/my_order?id=3" hover-class="none">
            <view class="icon iconfont">&#xe641;</view>
            <view class="name">待收货</view>
          </navigator>
          <navigator class="item" url="/pages/user/my_order?id=4" hover-class="none">
            <view class="icon iconfont">&#xe639;</view>
            <view class="name">评价</view>
          </navigator>
          <navigator class="item" url="/pages/user/order_after_sale" hover-class="none">
            <view class="icon iconfont">&#xe85d;</view>
            <view class="name">退款/售后</view>
          </navigator>
        </view>
      </view>
      <navigator class="account_module"  url="/pages/more_pages/login" hover-class="none">
        <view class="account_title">
          <text class="icon iconfont">&#xe786;</text>
          <text class="title">我的足迹</text>
          <view class="arrow_icon">
            <text class="icon iconfont">&#xe62e;</text>
          </view>
        </view>
        <view class="account_text">
          <view class="item">
            <view class="icon iconfont">&#xe608;</view>
            <view class="name">登录后查看</view>
          </view>
        </view>
      </navigator>
      <view class="account_module">
        <navigator class="account_title" url="/pages/user/install/main" hover-class="none">
          <text class="icon iconfont">&#xe73b;</text>
          <text class="title">我的服务</text>
          <view class="arrow_icon">
            <text class="icon iconfont">&#xe62e;</text>
          </view>
        </navigator>
        <view class="account_text">
          <navigator class="item" url="/pages/user/serve/notice"  hover-class="none">
            <view class="icon iconfont">&#xe60d;</view>
            <view class="name">商城公告</view>
          </navigator>
          <navigator class="item" url="/pages/user/serve/voucher_center"  hover-class="none">
            <view class="icon iconfont">&#xe60c;</view>
            <view class="name">领券中心</view>
          </navigator>
          <navigator class="item" url="/pages/user/serve/address"  hover-class="none">
            <view class="icon iconfont">&#xe641;</view>
            <view class="name">地址管理</view>
          </navigator>
        </view>
        <view class="account_text">
          <navigator class="item" url="/pages/user/serve/collection"  hover-class="none">
            <view class="icon iconfont">&#xe639;</view>
            <view class="name">我的收藏</view>
          </navigator>
          <view class="item">
            <view class="icon iconfont">&#xe85d;</view>
            <view class="name">分享</view>
          </view>
          <navigator class="item" url="/pages/user/serve/live_broadcast"  hover-class="none">
            <view class="icon iconfont">&#xe85d;</view>
            <view class="name">直播</view>
          </navigator>
        </view>
        <view class="account_text">
          <avigator class="account_title" url="/pages/user/install/main" hover-class="none">
            <view class="icon iconfont">&#xe639;</view>
            <view class="name">设置</view>
          </avigator>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.user_top {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 265rpx;
  padding: 100rpx 30rpx 0;
  position: relative;
  background: #fa436a;
  .user_info_box {
    height: 180rpx;
    width: 100%;
    z-index: 1;
    .user_info {
      display: flex;
      align-items: center;
      line-height: 180rpx;
      .photo_img {
        width: 130rpx;
        height: 130rpx;
        border: 5rpx solid #fff;
        border-radius: 50%;
      }
      .lod_text {
        font-size: 38rpx;
        color: #fff;
        margin-left: 20rpx;
      }
    }
  }
  .vip_card_box {
    display: flex;
    height: 240rpx;
    width: 90%;
    background: black;
    border-radius: 16rpx 16rpx 0 0;
    overflow: hidden;
    position: relative;
    padding: 20rpx 24rpx;
    .card_sign {
      position: absolute;
      right: 24rpx;
      top: 24rpx;
      width: 132rpx;
      height: 40rpx;
      font-size: 28rpx;
      text-align: center;
      color: #36343c;
      border-radius: 20px;
      background: linear-gradient(to left, #f9e6af, #ffd465);
      z-index: 1;
    }
    .vip_title {
      display: flex;
      width: 100%;
      color: #f7d680;
      height: 40rpx;
      line-height: 50rpx;
      .iconfont {
        display: inline;
        color: #f6e5a3;
        margin-right: 10rpx;
      }
      .vip_text {
        display: inline;
        font-size: 28rpx;
      }
    }
  }
}

.user_content {
  padding: 20rpx 30rpx 0 30rpx;
  position: relative;
  background-color: #f8f8f8;
  .arc {
    position: absolute;
    left: 0;
    top: -25rpx;
    height: 36rpx;
  }
  .account_module {
    background-color: #fff;
    margin-bottom: 20rpx;
    height: 200rpx;

    .account_title {
      display: flex;
      height: 50rpx;
      padding: 20rpx 30rpx;
      border-bottom: 1rpx solid #f8f8f8;
      position: relative;
      line-height: 70rpx;
      .iconfont {
        color: #fa436a;
        font-size: 50rpx;
        margin-right: 10rpx;
      }
      .title {
        font-size: 28rpx;
        color: #303133;
      }
      .arrow_icon {
        .iconfont {
          display: inline;
          position: absolute;
          right: 50rpx;
          font-size: 30rpx;
          color: #606266;
        }
      }
    }
  }
  .account_text {
    display: flex;
    justify-content: space-around;
    color: #606266;
    font-size: 22rpx;
    height: 130rpx;
    .item {
      text-align: center;
      margin: auto 0;
      .iconfont {
        font-size: 50rpx;
        color: #fa436a;
      }
    }
  }
}
</style>