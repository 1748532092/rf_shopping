<template>
  <view class="search_pages">
      <view class="search_box">
          <input class="input_text" placeholder="蔬菜"/>
          <text class="icon iconfont">&#xe647;</text>
          <button class="search_btn">搜索</button>
      </view>
      <view class="search_records">
         <view class="history_search">
             <view class="header">
                 <text class="title">历史搜索</text >
             <view class="icon iconfont">&#xe61d;</view>
             </view>
             <view class="content">
                 <view class="no_content">暂无记录</view>
             </view>
             
         </view>
          <view class="history_search">
             <view class="header">
                 <text class="title">热门搜索</text >
             <view class="icon iconfont">&#xe693;</view>
             </view>
             <view class="content">
                 <view class="data" v-for="(item,index) in list" >{{item}}</view>
             </view>
             
         </view>
             
         </view>
      </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      list: ["iphone", "小米", "华为", "面包机", "娃娃哈"],
    };
  },
};
</script>

<style lang="scss" scoped>
.search_pages {
  background: #f5f5f5;
  height: 100%;
  font-size: 28rpx;
  padding-top: 10rpx;
  .search_box {
    display: flex;
    position: relative;
    margin: 20rpx;
    border-radius: 2em;
    background: #fff;
    height: 60rpx;
    align-items: center;
    .input_text {
      width: 600rpx;
      padding-left: 60rpx;
    }
    .iconfont {
      position: absolute;
      left: 10rpx;
      font-size: 50rpx;
    }
    .search_btn {
      background: #fa436a;
      padding: 0 10rpx;
      width: 100rpx;
      height: 60rpx;
      display: inline-flex;
      font-size: 26rpx;
      line-height: 60rpx;
      color: #fff;
      justify-content: center;
      border-radius: 0 2em 2em 0;
      border: 1rpx solid #fff;
    }
  }
  .search_records {
    padding: 20rpx;
    background: #fff;
    .history_search {
      .header {
        display: flex;
        justify-content: space-between;
        .title {
        }
        .iconfont {
        }
      }
      .content {
                 text-align: left;
        margin: 20rpx 0;
        
        .no_content {
          color: #6b6b6b;
          text-align: center;
        }
        .data {
          display: inline-flex;
          flex-wrap: wrap;
          background: #f2f2f2;
          margin: 10rpx 20rpx 10rpx 0;
          padding: 0 20rpx;
          border-radius: 2em;
        }
      }
    }
  }
}
</style>