<!--
 * @Author: your name
 * @Date: 2021-04-26 09:15:33
 * @LastEditTime: 2021-04-26 13:52:48
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\screen.vue
-->
<template>
  <view>
      <view class="header">
            <!-- 状态栏占位 -->
    <view
      class="statusBar"
      :style="{ paddingTop: statusBarHeight + 'px' }"
    ></view>
    <view class="search_scan">
      <text class="icon iconfont">&#xe61b;</text>
      <view class="search_box">
        <view class="search_img">
          <view class="icon iconfont">&#xe647;</view>
        </view>
        <input class="input_text" placeholder="请输入关键字" />
      </view>
    </view>
    <view class="filter_bar">
        <view>综合</view>
        <view>销量</view>
        <view class="icon iconfont">&#xe62d;</view>
        <view>筛选5</view>
    </view>
      </view>
  
  </view>
</template>

<script>
export default {
  data() {
    return {
      // 状态栏高度
      statusBarHeight: 0,
    };
  },
  //第一次加载时调用
  created() {
    //获取手机状态栏高度
    this.statusBarHeight = uni.getSystemInfoSync()["statusBarHeight"];
  },
};
</script>

<style lang="scss" scoped>
.header{
    .search_scan {
  display: flex;
  justify-content: space-around;
  align-items: center;
  vertical-align: middle;
  height: 60rpx;
  width: 530rpx;
  padding-top: 20rpx;
  margin-bottom: 20rpx;
  .search_box {
    display: flex;
    position: relative;
    background: #f5f5f5;
    height: 60rpx;
    width: 80%;
    border-radius: 2em;
    align-items: center;
    padding: auto 10rpx;
    .input_text {
        font-size: 26rpx;
        color: #606266;
        margin-left: 20rpx;
      }
    .search_img {
     
      .iconfont {
           display: inline-flex;
        color: rgb(153, 141, 141);
        align-items: center;
        position: absolute;
        right: 20rpx;
        bottom: 0;
      }
    }
  }
}
.filter_bar{

}
}

</style>