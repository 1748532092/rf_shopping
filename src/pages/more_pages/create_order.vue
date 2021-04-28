<!--
 * @Author: your name
 * @Date: 2021-04-27 09:13:08
 * @LastEditTime: 2021-04-28 18:04:17
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\create_order.vue
-->
<template>
  <view>
    <view class="choose_address">
      <view class="left">
        <text class="icon iconfont">&#xe67c;</text>
      </view>
      <view class="middle">
        <view class="first_line">
          <text class="name">145</text>
          <text class="num">12345678901</text>
        </view>
        <view class="address">河北省 石家庄 长安区 长乐</view>
      </view>
      <view class="right">
        <text class="icon iconfont">&#xe62e;</text>
      </view>
    </view>
    <view class="product_list">
      <view class="header">
        <image class="logo" src="../../static/logo.png"></image>
        <text class="tit">商品列表</text>
      </view>
      <view class="content">
        <image class="product_img" src="../../static/goods.jpg"></image>
        <view class="right">
          <view class="product_name">狗狗零食</view>
          <view class="type">大包 孜然 *1</view>
          <view class="price">¥ 100.00</view>
        </view>
      </view>
    </view>
    <view class="list">
      <view class="list_cell">
        <view class="cell_icon">券</view>
        <text class="cell_tit">优惠券</text>
        <text class="cell_tip">选择优惠券</text>
      </view>
      <view class="list_cell">
        <view class="cell_icon">寄</view>
        <text class="cell_tit">配送方式</text>
        <text class="cell_tip">物流配送</text>
      </view>
      <view class="list_cell">
        <view class="cell_icon">递</view>
        <text class="cell_tit">快递公司</text>
        <text class="cell_tip">中通</text>
      </view>
    </view>
    <view class="list">
      <view class="list_cell">
        <text class="cell_tit">商品总价</text>
        <text class="cell_tip">¥5699.00</text>
      </view>
      <view class="list_cell">
        <text class="cell_tit">运费</text>
        <text class="cell_tip">¥0</text>
      </view>
      <navigator class="list_cell"
        url="/pages/user/install/invoices"
        hover-class="none">
        <text class="cell_tit">开具发票</text>
        <text class="cell_inv">本次不开具发票</text>
      </navigator>
      <view class="list_cell"
      >
        <text class="cell_tit">备注</text>
        <text class="cell_desc">请填写备注信息</text>
      </view>
    </view>
    <view class="footer">
      <view class="price_content">
        <text class="price_tit">实付款：</text>
        <text class="price_icon">¥</text>
        <text class="price">100.00</text>
      </view>
      <navigator class="sub_btn" url="/pages/more_pages/payment"
        >提交订单</navigator
      >
    </view>
  </view>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.choose_address {
  display: flex;
  align-items: center;
  padding: 30rpx 0;
  position: relative;
  background: #fff;
  border-bottom: 1rpx dashed rgb(208, 219, 223);
  .left {
    margin: 0 20rpx;
    width: 90rpx;
  }
  .middle {
    color: #303133;
    .first_line {
      .name {
        font-size: 34rpx;
        margin-right: 24rpx;
      }
      .num {
        font-size: 28rpx;
      }
    }
    .address {
      font-size: 28rpx;
      color: #888;
      margin-top: 20rpx;
    }
  }
  .right {
    position: absolute;
    right: 50rpx;
  }
}
.product_list {
  margin: 20rpx 30rpx;
   background: #fff;
  .header {
    display: flex;
    align-items: center;
    height: 84rpx;
    padding: 0 30rpx;
    position: relative;
    .logo {
      border-radius: 50rpx;
      width: 50rpx;
      height: 50rpx;
      margin-right: 30rpx;
    }
    .tit {
      font-size: 32rpx;
    }
  }
  .content {
    display: flex;
    font-size: 28rpx;
    .product_img {
      width: 220rpx;
      height: 170rpx;
      border-radius: 4rpx;
    }
    .right {
      margin-left: 16rpx;
      .type {
        color: #888;
        margin: 10rpx 0;
      }
      .price {
        color: #fa436a;
      }
    }
  }
}
.list {
  margin-top: 16rpx;
  background: #fff;
  font-size: 28rpx;
  .list_cell {
    display: flex;
    align-items: center;
    padding: 10rpx 30rpx 20rpx 40rpx;
    position: relative;
    border-bottom: 1rpx solid #f8f8f8;
    height: 65rpx;
    .cell_icon {
      height: 32rpx;
      width: 32rpx;
      text-align: center;
      border-radius: 4rpx;
      background: #fa436a;
      color: #fff;
      margin-right: 15rpx;
      font-size: 24rpx;
    }
    .cell_tit {
      color: #888;
    }
    .cell_tip {
      color: #fa436a;
      position: absolute;
      right: 30rpx;
    }
    .cell_inv {
      position: absolute;
      right: 30rpx;
    }
    .cell_desc {
      font-size: 28rpx;
      color: #888;
      margin-left: 30rpx;
    }
  }
}
.footer {
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 80rpx;
  justify-content: space-between;
  align-items: center;
  .price_content {
    padding: 30rpx;
    .price_tit {
      font-size: 30rpx;
    }
    .price_icon {
      font-size: 24rpx;
      color: #fa436a;
    }
    .price {
      font-size: 32rpx;
      color: #fa436a;
    }
  }
  .sub_btn{
      text-align: center;
      line-height: 80rpx;
      background: #fa436a;
      height: 80rpx;
      width: 280rpx;
      border-radius: 4rpx;
      font-size: 32rpx;
      color: #fff;
  }
}
</style>