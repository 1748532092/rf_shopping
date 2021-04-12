
<template>
  <view>
    <view class="home_page_top">
      <view class="search_scan">
        <view>
          <input class="input_box" placeholder="蔬菜" />
          <view class="search_img">
            <image class="iconfont iconsousuo"></image>
          </view>
        </view>
        <view>
          <image></image>
        </view>
      </view>
      <scroll-view class="tab_list" scroll-x scroll-with-animation>
        <view class="tab_item">家用电器</view>
        <view class="tab_item">手机数码</view>
        <view class="tab_item">玩具乐器</view>
        <view class="tab_item">钟表珠宝</view>
        <view class="tab_item">家用电器</view>
        <view class="tab_item">手机数码</view>
        <view class="tab_item">玩具乐器</view>
        <view class="tab_item">钟表珠宝</view>
      </scroll-view>
    </view>
	<!-- banner -->
	<view class="home_page_banner">
		<image class = "banner_img" src ="../../static/share/banner_one.png"></image>
	</view>
  </view>
</template>

<script>
export default {
  data: {
    curTab: 0,
    current: 0,
    tabList: [
      {
        id: 1,
        name: "家用电器",
      },
      {
        id: 2,
        name: "手机数码",
      },
      {
        id: 3,
        name: "玩具乐器",
      },
      {
        id: 4,
        name: "钟表珠宝",
      },
    ],
  },
  selectTab(e) {
    let index = e.target.dataset.index;
    this.setDate({
      curTab: index,
      current: index,
    });
  },
  swiperChange(e) {
    let index = e.detail.index;
    this.setDate({
      curTab: index,
      current: index,
    });
  },
};
</script>

<style lang="less" scoped>
.home_page_top {
  background: #fa436a;
  height: 250rpx;
  .search_scan {
    display: flex;
    justify-content: space-around;
    height: 60rpx;
    width: 80%;
    padding-top: 65rpx;
    margin-bottom: 20rpx;
    .input_box {
      flex: 1;
      background: #fff;
      height: 60rpx;
      width: 100%;
      border-radius: 2em;
      .search_img {
        position: absolute;
        left: 50%;
        top: 50%;
        z-index: 2;
      }
      .input_text {
        font-size: 16rpx;
        line-height: 1;
      }
    }
  }
  .tab_list {
    width: 100%;
    height: 88rpx;
    border-bottom: 1rpx solid #e5e5e5;
    display: inline-block;
    white-space: nowrap;
    .tab_item {
      width: 140rpx;
      height: 85rpx;
      display: inline-block;
      line-height: 85rpx;
      vertical-align: middle;
      text-align: center;
      margin: 0rpx 20rpx 10rpx 10rpx;
    }
    //切换时下划线
    .selected_tab {
      color: #1aae18;
      border-bottom: 5rpx solid #1aae18;
    }
  }
  .home_page_banner{
	
	  .banner_img{
		  height: 350rpx;
	 	 width:100rpx;
		  border-radius: 2em;
	  }
  }
}
</style>