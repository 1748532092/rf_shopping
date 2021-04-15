<!--
 * @Author: your name
 * @Date: 2021-04-12 15:44:10
 * @LastEditTime: 2021-04-15 18:16:53
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\cart\cart.vue
-->
<template>
  <view class="unlog_cart">
      <view class="icon iconfont">&#xe697;</view>
      <view class="txt">
          <text class="empty_text">空空如也</text>
          <text class="lod_text">登录/注册></text>
      </view>
  </view>
</template>

<script>
export default {

}
</script>

<style lang="less" scoped>
.unlog_cart{
    padding-top: 50%;
    .iconfont{
        font-size: 150rpx;
        color: red;
        text-align: center;
    }
    .txt{
        margin-top: 20rpx;
        font-size: 26rpx;
        text-align: center;
        .empty_text{
            color:rgb(204, 197, 197);
    }
    .lod_text{
           margin-left: 10rpx;
            color: rgb(238, 66, 75);
    }
    }
    
}
</style>