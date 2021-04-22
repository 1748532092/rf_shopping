
<template>
  <view class="my_order">
    <view class="search_box">
      <view class="search_input">请输入订单关键字</view>
      <text class="icon iconfont">&#xe647;</text>
    </view>
    <view>
      <scroll-view scroll-x="true" scroll-with-animation class="scroll_tab">
        <block v-for="(item, index) in tabBars" :key="index">
          <view
            :class="{ active: tabIndex == index }"
             class="scroll_tab_item"
            @click="toggleTab(index)"
          >
            {{ item.name }}
            <!-- <view class="scroll_tab_line"></view> -->
          </view>
        </block>
      </scroll-view>
    </view>
    <swiper class="swiper_box" :current="tabIndex" @change="tabChange">
      <swiper-item class="item">
        <scroll-view scroll-y="true" class="content">
          <empty></empty>
        </scroll-view>
      </swiper-item>
      <swiper-item class="item">
        <scroll-view scroll-y="true" class="content">
          <empty></empty>
        </scroll-view>
      </swiper-item>
      <swiper-item class="item">
        <scroll-view scroll-y="true" class="content">
          <empty></empty>
        </scroll-view>
      </swiper-item>
      <swiper-item class="item">
        <scroll-view scroll-y="true" class="content">
          <empty></empty>
        </scroll-view>
      </swiper-item>
      <swiper-item class="item">
        <scroll-view scroll-y="true" class="content">
          <empty></empty>
        </scroll-view>
      </swiper-item>
    </swiper>
  </view>
</template>
<script>
import empty from "../../components/empty_order.vue";
export default {
  components: {
    empty,
  },
  onLoad(e){
   this.tabIndex=e.id
  },
  data() {
    return {
      tabIndex: 0 /* 选中标签栏的序列,默认显示第一个 */,
      tabBars: [
        {
          id: "1",
          name: "全部",
        },
        {
          id: "2",
          name: "待付款",
        },
        {
          id: "3",
          name: "待发货",
        },
        {
          id: "4",
          name: "待收货",
        },
        {
          id: "5",
          name: "评价",
        },
      ],
    };
  },
  methods: {
    //切换选项卡
    toggleTab(index) {
      this.tabIndex = index;
    },
    //滑动切换swiper
    tabChange(e) {
      console.log(e);
      this.tabIndex = e.detail.current;
    },
  },
};
</script>
<style lang="scss" scoped>

.my_order {
  background: #f8f8f8;
  height: 100%;
  font-size: 28rpx;
  .search_box {
    padding: 10rpx 20rpx;
    position: relative;
    height: 48rpx;
    line-height: 48rpx;
    margin-bottom: 20rpx;
    .search_input {
      width: 100%;
      background-color: #fff;
      border-radius: 40rpx;
      padding: 10rpx 0 10rpx 30rpx;
      color: #909399;
    }
    .iconfont {
      position: absolute;
      right: 48rpx;
      top: 22rpx;
      font-size: 50rpx;
    }
  }
  .active {
    color: #fa436a ;
    border-bottom: 5rpx solid #fa436a;
  }
  .scroll_tab {
    white-space: nowrap; /* 必要，导航栏才能横向*/
    height: 80rpx;
    background: #fff;
    margin: 10rpx auto;
  }
  .scroll_tab_item {
    display: inline-block; /* 必要，导航栏才能横向*/
    margin: 10rpx 25rpx 0rpx 30rpx;
    font-size: 36rpx;
  //  color: rgb(54, 49, 49);
    height: 50rpx;
    text-align: center;
  }

  .swiper_box {
    height: calc(100% - 170rpx);
    .item{
      overflow: auto;
    }
    .content {
      height: 100%;
    }
  }
}
</style>