<!--
 * @Author: your name
 * @Date: 2021-04-14 09:03:28
 * @LastEditTime: 2021-04-15 17:01:50
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\components\men_cloth.vue
-->

<template name="clothTab">
  <view class="new_products_modules">
    <view class="new_products_content">
      <view class="goods_item" v-for="items in 4" :key="items">
        <view class="show_img">
          <image class="goods_img" src="../static/goods.jpg"></image>
          <image class="goods_label" src="../static/pinkage.png"></image>
        </view>
        <view class="goods_name"
          >狗狗零食牛肉粒补钙除口臭训狗奖励小泰迪金毛幼犬小狗狗</view
        >
        <view style="margin-top: 20rpx">
          <view class="selling_price">
            <view class="selling_price_sign">¥</view>
            <view class="selling_price_text">38</view>
          </view>
          <view class="original_price">
            <view class="original_price_sign">¥</view>
            <view class="original_price_text">45</view>
          </view>
        </view>
        <view class="goods_sales">
          <view style="display: inline">
            <span>301</span>
            <view class="sales_number">人付款</view>
          </view>
          <view class="icon iconfont">&#xe602; </view>
        </view>
      </view>
    </view>
    <view class="nomore_text">没有更多了</view>
  </view>
</template> 
    <<script >
    
    export default {
        
    }
    </script>

    <<style lang="scss" scoped>
    .new_products_modules {
  .new_products_content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    .goods_item {
      margin-top: 30rpx;
      .show_img {
        display: flex;
        height: 300rpx;
        width: 300rpx;
        position: relative;
        .goods_img {
          height: 300rpx;
          width: 300rpx;
          margin: auto;
        }
        .goods_label {
          height: 50rpx;
          width: 50rpx;
          position: absolute;
          top: 0;
          left: 0;
        }
      }
      .goods_name {
        height: 50rpx;
        width: 300rpx;
        font-size: 28rpx;
        overflow: hidden;
        text-overflow: ellipsis; //当对象内文本溢出时显示省略标记
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
        padding: 20rpx;
      }
      .selling_price{
        display: inline-flex;
        margin-right: 10rpx;
        padding-left:20rpx;
        .selling_price_sign{
          display: inline;
          font-size: 32rpx;
          color: red;
        }
        .selling_price_text{
          display: inline;
          font-size: 30rpx;
          color: red;
        }
      }
      .original_price{
        display: inline-flex;
        text-decoration: line-through;
        .original_price_sign{
          display: inline;
          font-size: 28rpx;
          color: rgb(124, 112, 112);
        }
        .original_price_text{
          display: inline;
          font-size: 26rpx;
          color: rgb(124, 112, 112);
          margin-left: 10rpx;
        }
      }
      .goods_sales{
        position: relative;
        width: 300rpx;
        padding: auto 20rpx;
        span{
            color: red;
             font-size: 26rpx;
          }
        .sales_number{
          display: inline;
          font-size: 26rpx;
        }
        .iconfont{
          position: absolute;
          right: 0;
          display: inline;
          font-size: 50rpx;
          color: red;
        }
      }
    }
  }
 .nomore_text{
      font-size:30rpx;  
      color: rgb(80, 75, 75);
      margin-top:50rpx;
      text-align:center;
  }
}
    </style>