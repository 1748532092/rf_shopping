<!--
 * @Author: your name
 * @Date: 2021-04-27 09:13:08
 * @LastEditTime: 2021-04-27 15:53:24
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
  </view>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .choose_address{
      display: flex;
      align-items: center;
      margin-top: 30rpx;
      .left{
          margin: 0 20rpx;
      }
      .middle{
          .first_line{

          }

      }
      .right{

      }
  }
</style>