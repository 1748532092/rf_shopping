<!--
 * @Author: your name
 * @Date: 2021-04-21 15:42:17
 * @LastEditTime: 2021-04-21 17:43:53
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\product_details.vue
-->
<template name="product_details">
  <view class="product_details">
      <text class="back_btn icon iconfont">&#xe628;</text>
      <view class="product_img">
          <swiper>
            <swiper-item class="swiper_item">
              <image src="../static/goods.jpg"></image>
              <view class="tag">
                1/1
              </view>
            </swiper-item>
          </swiper>
      </view>
      <!-- 商品信息 -->
      <view class="product_information">
        <view class="introduce_first_line">
          <view>
            
          </view>
        </view>
      </view>
  </view>
</template>

<script>
export default {

}
</script>

<style lang="less" scoped>
.product_details{
  .back_btn{
   font-size: 40rpx;
   position: fixed;
   padding-top: 100rpx;
   left: 40rpx;
   top: 40rpx;
   z-index: 3;
  }
  .product_img{
    height: 722rpx;
		position: relative;
    swiper{
      height: 100%;
    }
    .swiper_item{
      display: flex;
			justify-content: center;
			align-content: center;
			height: 750rpx;
			overflow: hidden;
			border-bottom: 1rpx solid rgba(0, 0, 0, 0.01);
      image{
        width: 100%;
        height: 100%;
    }
    .tag{
      background: #fa436a;
      color: #fff;
      position: absolute;
      bottom: 20rpx;
      right: 20rpx;
      font-size: 24rpx;
      border-radius: 2em;
      padding: 0 28rpx;
    }
    }
    
  }
}
</style>