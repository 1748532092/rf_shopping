<!--
 * @Author: your name
 * @Date: 2021-04-25 17:53:38
 * @LastEditTime: 2021-04-25 17:53:51
 * @LastEditors: your name
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\bill_details.vue
-->
<template>
  <view>
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
      <swiper-item class="item" v-for="(item, index) in tabBars" :key="index">
        <swiper-view class="content">
          <empty_bill_details></empty_bill_details>
        </swiper-view>
      </swiper-item>
    </swiper>
  </view>
</template>

<script>
import empty_bill_details from "../../components/empty_bill_details";
export default {
  components: {
    empty_bill_details,
  },
  data() {
    return {
      tabIndex: 0 /* 选中标签栏的序列,默认显示第一个 */,
      tabBars: [
        {
          id: "0",
          name: "全部",
        },
        {
          id: "1",
          name: "充值",
        },
        {
          id: "2",
          name: "消费",
        },
      ],
    };
  },
  methods: {
    //切换选项卡
    toggleTab(index) {
      this.tabIndex = index;
      console.log(this.tabIndex)
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
.active {
  color: #fa436a;
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
  margin: 10rpx 90rpx 0rpx;
  font-size: 36rpx;
  height: 50rpx;
  text-align: center;
}

.swiper_box {
  height: calc(100vh - 170rpx);
  .item {
    overflow: auto;
  }
  .content {
    height: 100%;
  }
}
</style>