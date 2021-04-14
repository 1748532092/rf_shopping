
<template>
  <view>
    <view class="home_page_top">
      <!-- 状态栏占位 -->
      <view
        class="statusBar"
        :style="{ paddingTop: statusBarHeight + 'px' }"
      ></view>
      <view class="search_scan">
        <view class="search_box">
          <view class="search_img">
            <view class="icon iconfont">&#xe647;</view>
          </view>
          <input class="input_text" placeholder="蔬菜" />
        </view>
        <view class="scan_img">
          <text class="icon iconfont">&#xe78d;</text>
        </view>
      </view>
      <view>
        <scroll-view scroll-x="true" scroll-with-animation class="scroll_tab">
          <block v-for="(item, index) in tabBars" :key="index">
            <view
              class="scroll_tab_item"
              :class="{ active: tabIndex == index }"
              @click="toggleTab(index)"
            >
              {{ item.name }}
              <view class="scroll_tab_line"></view>
            </view>
          </block>
        </scroll-view>
      </view>

      <!-- 内容区 -->
      <view class="content">
        <!-- 滑块视图 -->
        <swiper style="height:4000rpx"  :current="tabIndex" @change="tabChange"
          ><!-- current:当前所在滑块的index -->
          <!-- <swiper-item v-for="(content, index) in contentList" :key="index">
            <view class="content">{{ content }}</view>
          </swiper-item> -->
          <swiper-item class="home_page_content">
            <scroll-view scroll-x="true" style="height:100%"> 
              <homeTab></homeTab>
            </scroll-view>
            
          </swiper-item>
          <swiper-item>
            <electricTab></electricTab>
          </swiper-item>
          <swiper-item>
            <clothTab></clothTab>
          </swiper-item>
          <swiper-item>
            <phoneTab></phoneTab>
          </swiper-item>
        </swiper>
      </view>
    </view>
   
  </view>
</template>

<script>
import electricTab from "../../components/electric";
import homeTab from "../../components/home_page_tab";
import clothTab from "../../components/men_cloth";
import phoneTab from "../../components/phone";
export default {
  components: {
    electricTab,
    homeTab,
    clothTab,
    phoneTab,
  },
  data() {
    return {
      // 状态栏高度
      statusBarHeight: 0,
      tabIndex: 0 /* 选中标签栏的序列,默认显示第一个 */,
      contentList: ["首页", "家电用器", "男装", "手机"],
      tabBars: [
        {
          id: "1",
          name: "首页",
        },
        {
          id: "2",
          name: "家电用器",
        },
        {
          id: "3",
          name: "男装",
        },
        {
          id: "4",
          name: "手机",
        },
      ],
    };
  }, //第一次加载时调用
  created() {
    //获取手机状态栏高度
    this.statusBarHeight = uni.getSystemInfoSync()["statusBarHeight"];
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

<style lang="less" scoped>
.home_page_top {
  background: #fa436a;
  height: 200rpx;
  .search_scan {
    display: flex;
    justify-content: space-around;
    vertical-align: middle;
    height: 60rpx;
    width: 550rpx;
    padding-top: 10rpx;
    margin-bottom: 20rpx;
    .search_box {
      display: flex;
      background: #fff;
      height: 60rpx;
      width: 100%;
      border-radius: 2em;
      margin-left: 20rpx;
      .input_text {
        font-size: 26rpx;
        margin: auto 0rpx;
      }
      .search_img {
        display: inline-flex;
        align-items: center;
        margin-left: 175rpx;
        margin-right: 10rpx;
        .iconfont {
          font-size: 50rpx;
          color: rgb(153, 141, 141);
        }
      }
    }
    .scan_img {
      .iconfont {
        line-height: 60rpx;
        font-size: 70rpx;
        color: white;
        margin-left: 5rpx;
      }
    }
  }
  .active {
    color: #fff;
    border-bottom: 5rpx solid white;
  }
  .scroll_tab {
    white-space: nowrap; /* 必要，导航栏才能横向*/
  }
  .scroll_tab_item {
    display: inline-block; /* 必要，导航栏才能横向*/
    margin: 10rpx 25rpx 0rpx 25rpx;
    font-size: 28rpx;
    color: #fff;
    height: 47rpx;
    text-align: center;
  }
}
.content{
  margin-top: 50rpx;
  .home_page_content{
     height: 350rpx;
  }
}
</style>