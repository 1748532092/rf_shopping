<template>
  <view class="install_page">
    <view class="list_item" v-for="(item,index) in list" :key="index">
      <text class="item_title">{{item}}</text>
      <text class="item_tip"></text>
      <text class="icon iconfont">&#xe62e;</text>
    </view>
    <view class="choose_color">
      <view class="item">
        <view class="content">
          <text class="icon iconfont">&#xe644;</text>
          <view class="color"></view>
          <view class="title"
            >主题色：
            <text style="color: #fa436a">官方</text>
          </view>
        </view>
        <view>
          <button class="choose_btn">
            <text class="icon iconfont">&#xe644;</text>
            <text>选择主题</text>
          </button>
        </view>
      </view>
    </view>
    <view class="log_out">
        <text class="btn_text">退出登录</text>
    </view>
  </view>
</template>
<script>
export default {
  data(){
    return{
      list:["个人资料","修改密码","授权管理","发票管理","开票历史","清楚缓存","关于商城","站点帮助","意见反馈"]
    }
  }
};
</script>
<style lang="less" scoped>
.install_page {
  background: #f8f8f8;
  padding: 20rpx 0;
  .m_t {
    margin-top: 20rpx;
  }
  .list_item {
    display: flex;
    height: 60rpx;
    line-height: 60rpx;
    padding: 20rpx 30rpx;
    position: relative;
    background: #fff;
    justify-content: center;
    border-bottom: 1px solid #e4e7ed;
    &:nth-child(3n){
      margin-bottom: 20rpx;
    }
    .item_title {
      flex: 1;
      font-size: 30rpx;
      margin-left: 10rpx;
    }
    .item_tip {
      font-size: 28rpx;
      color: #909399;
    }
    .iconfont {
      color: #909399;
      margin-left: 10rpx;
    }
  }
  .choose_color {
    display: block;
    overflow: hidden;
    margin: 20rpx 30rpx;
    border-radius: 20rpx;
    .item {
      position: relative;
      display: flex;
      padding: 0 30rpx;
      min-height: 100rpx;
      background-color: #ffffff;
      justify-content: space-between;
      align-items: center;
      .content {
        display: flex;
        font-size: 30rpx;
        align-items: center;
        .iconfont {
          color: #fa436a;
          display: inline-block;
          margin-right: 10rpx;
          width: 1.6rpx;
          text-align: center;
        }
        .color {
          background-color: #fa436a;
          width: 50rpx;
          height: 50rpx;
          border-radius: 6rpx;
          margin-right: 20rpx;
        }
        .title {
          font-size: 28rpx;
        }
      }
      .choose_btn {
        border-radius: 2em;
        position: relative;
        border: 0rpx;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        padding: 0 30rpx;
        font-size: 28rpx;
        height: 64rpx;
        line-height: 1;
        text-align: center;
        text-decoration: none;
        background-color: #fa436a;
        color: #fff;
        .iconfont{
            color: #fa436a;
            font-size: 28rpx;
        }
      }
    }
  }
  .log_out{
      display: flex;
      padding: 20rpx 30rpx;
      position: relative;
      background: #fff;
      justify-content: center;
      margin: 40rpx 0;
      .btn_text{
          flex: 1;
          font-size: 30rpx;
          color: #fa436a;
          text-align: center;
      }
  }
}
</style>