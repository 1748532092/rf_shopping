<!--
 * @Author: your name
 * @Date: 2021-04-12 15:44:49
 * @LastEditTime: 2021-04-25 16:03:58
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\news\news.vue
-->
<template>
  <view class="unlog_cart">
      <view class="icon iconfont">&#xe637;</view>
      <view class="txt">
          <text class="empty_text">暂未登录</text>
          <navigator class="lod_text" url="/pages/more_pages/login" hover-class="none">登录/注册></navigator>
      </view>
  </view>
</template>

<script>

export default {}
	

</script>

<style lang="scss" scoped>
.unlog_cart{
    padding-top: 50%;
    .iconfont{
        font-size: 150rpx;
        color: red;
        text-align: center;
    }
    .txt{
        display: flex;
        margin-top: 20rpx;
        font-size: 26rpx;
        text-align: center;
        justify-content: center;
        .empty_text{
            color:rgb(204, 197, 197);
    }
    .lod_text{
           margin-left: 10rpx;
            color: rgb(238, 66, 75);
    }
    }}
</style>