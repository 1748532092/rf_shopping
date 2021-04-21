<!--
 * @Author: your name
 * @Date: 2021-04-21 14:41:16
 * @LastEditTime: 2021-04-21 15:38:00
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\serve\live_broadcast.vue
-->
<template>
  <view class="my_order">
 
    <view>
      <scroll-view scroll-x="true" scroll-with-animation class="scroll_tab">
        <block v-for="(item, index) in tabBars" :key="index">
          <view
            :class="{ active: tabIndex == index }"
             class="scroll_tab_item"
            @click="toggleTab(index)"
          >
            {{ item.name }}
          </view>
        </block>
      </scroll-view>
    </view>
    <swiper class="swiper_box" :current="tabIndex" @change="tabChange">
      <swiper-item class="item" v-for="(item,index) in tabBars" :key="index">
        <scroll-view scroll-y="true" class="content">
          <empty_live_broadcast></empty_live_broadcast>
        </scroll-view>
      </swiper-item>
    </swiper>
  </view>
</template>
<script>
import empty_live_broadcast from "../../../components/empty_live_broadcast.vue";
export default {
  components: {
    empty_live_broadcast
  },
  data() {
    return {
      tabIndex: 0 /* 选中标签栏的序列,默认显示第一个 */,
      tabBars: [
        {
          id: "1",
          name: "进行中",
        },
        {
          id: "2",
          name: "未开始",
        },
        {
          id: "3",
          name: "已结束",
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
<style lang="less" scoped>

.my_order {
  background: #f8f8f8;
  height: 100%;
  font-size: 28rpx;
  .active {
    color: #fa436a ;
    border-bottom: 5rpx solid #fa436a;
  }
  .scroll_tab {
    white-space: nowrap; /* 必要，导航栏才能横向*/
    height: 80rpx;
    background: #fff;
    margin: 10rpx auto;
   display: flex;
   text-align: center;
  }
  .scroll_tab_item {

    display: inline-block; /* 必要，导航栏才能横向*/
    margin: 10rpx 70rpx; 
    font-size: 36rpx;
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