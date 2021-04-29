<!--
 * @Author: your name
 * @Date: 2021-04-12 15:44:10
 * @LastEditTime: 2021-04-29 15:49:26
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\cart\cart.vue
-->
<template>
  <!-- <view class="unlog_cart">
      <view class="icon iconfont">&#xe697;</view>
      <view class="txt">
          <text class="empty_text">空空如也</text>
          <navigator class="lod_text" url="/pages/more_pages/login" hover-class="none">登录/注册></navigator>
      </view>
  </view> -->
  <view class="cart_pages">
    <view class="goodsList">
      <view class="item">
        <view class="left">
          <view class="check_box"></view>
        </view>
        <view class="middle">
          <view>
            <image class="goods_img" src="../../static/goods.jpg"></image>
          </view>
          <view class="goods_inf">
            <view class="goods_name">狗狗零食</view>
            <view class="goods_type">大包</view>
            <view class="goods_price_number">
              <view class="price">¥100.00</view>
              <u-number-box
                class="number"
                v-model="value"
                @change="valChange"
              ></u-number-box>
            </view>
          </view>
        </view>
      </view>
    </view>
    <view class="footer">
        <view class="left">

        </view>
        <view class="right">

        </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      value: 1,
    };
  },
  methods: {
    valChange(e) {
      console.log("当前值为: " + e.value);
    },
  },
};
</script>

<style lang="scss" scoped>
.cart_pages {
  background: coral;
  height: 100%;
  .goodsList {
    .item {
      display: flex;
      width: calc(95%);
      height: calc(22vw + 40rpx);
      margin: 20rpx auto;
      border-radius: 15rpx;
      align-items: center;
      position: relative;
      background: #fff;
      .left {
        padding-left: 20rpx;
        height: 22vw;
        margin-right: 20rpx;
        display: flex;
        justify-content: center;
        align-items: center;
        .check_box {
          width: 35rpx;
          height: 35rpx;
          border-radius: 100%;
          border: 2rpx solid #fa436a;
        }
      }
      .middle {
        width: 100%;
        display: flex;
        .goods_img {
          width: 22vw;
          height: 22vw;
        }
        .goods_inf {
          padding-left: 20rpx;
          font-size: 26rpx;
          .goods_name {
          }

          .goods_type {
            margin-top: 45rpx;
            height: 40rpx;
            line-height: 40rpx;
            background: rgb(204, 201, 201);
            text-align: center;
            color: rgb(122, 121, 121);
            border-radius: 2em;
          }

          .goods_price_number {
            display: flex;
            margin-top: 10rpx;
            align-items: center;
            .price {
            }
            .number {
              position: absolute;
              right: 20rpx;
            }
          }
        }
      }
    }
  }
}
// .unlog_cart{
//     padding-top: 50%;
//     .iconfont{
//         font-size: 150rpx;
//         color: red;
//         text-align: center;
//     }
//     .txt{
//         margin-top: 20rpx;
//         font-size: 26rpx;
//         text-align: center;
//         display: flex;
//         justify-content: center;
//         .empty_text{
//             color:rgb(204, 197, 197);
//     }
//     .lod_text{
//            margin-left: 10rpx;
//             color: rgb(238, 66, 75);
//     }
//     }

// }
</style>