<!--
 * @Author: your name
 * @Date: 2021-04-23 08:54:03
 * @LastEditTime: 2021-04-23 15:08:57
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\more_pages\points_details.vue
-->
<template>
  <view class="points_details">
    <view class="header">
      <view class="title">当前积分</view>
      <text class="current_num">0</text>
      <view class="line"></view>
      <view class="navigation">
        <view class="item">
          <text class="points">0</text>
          <text class="title">累计积分</text>
        </view>
        <view class="item">
          <text class="points">0</text>
          <text class="title">累计消费</text>
        </view>
        <view class="item">
          <text class="points">0</text>
          <text class="title">冻结积分</text>
        </view>
      </view>
      <view class="tab">
        <!-- 头部 -->
        <view class="tab_header">
          <view
            :class="navIndex ==1 ? 'item active' :'item'"
            @click="checkIndex(1)"
            >分值明细</view
          >
          <view
            :class="navIndex ==2 ? 'item active' :'item'"
            @click="checkIndex(2)"
            >分值提升</view
          >
        </view>
      </view>
    </view>
    <!-- 内容 -->
    <view class="tab_contenet">
      <score_details class="show" v-if="navIndex == 1"></score_details>
      <score_increase class="show" v-if="navIndex == 2"></score_increase>
    </view>
  </view>
</template>
<script>
import score_details from "../../components/score_details";
import score_increase from "../../components/score_increase";
export default {
  components: {
    score_details,
    score_increase,
  },
  data() {
    return {
      navIndex: 1,
      navList: ["分值明细", "分值提升"],
      listIndex: 0,
    };
  },
  methods: {
    checkIndex(index) {
      this.navIndex = index;
    },
    checkListIndex(index) {
      this.listIndex = index;
    },
    

  },
};
</script>

<style lang="scss" scoped>
.points_details {
  .header {
    width: 100%;
    height: 420rpx;
    background: #fa436a;
    color: white;
    padding: 20rpx 0;
    text-align: center;
    position: relative;
    font-size: 28rpx;
    .title {
    }
    .current_num {
      margin-top: 10rpx;
      font-size: 50rpx;
    }
    .line {
      width: 10%;
      height: 3rpx;
      background-color: #fff;
      margin: 20rpx auto 30rpx;
    }
    .navigation {
      display: flex;
      width: 100%;
      .item {
        flex: 1;
        display: flex;
        flex-direction: column;
        .points {
          font-size: 34rpx;
        }
        .title {
        }
      }
    }
  }
  .tab {
    .tab_header {
      position: absolute;
      bottom: -2rpx;
      display: flex;
      width: 600rpx;
      margin: 0 10%;
      border-radius: 20rpx 20rpx 0 0;
      background-color: #f7f7f7;
      height: 80rpx;
      .item {
        width: 300rpx;
        display: inline-block;
        text-align: center;
        line-height: 80rpx;
        color: #bbb;
        border-radius: 20rpx 20rpx 0 0;
      }
      .active {
        color: #fa436a;
        background: #fff;
        border-radius: 20rpx 0 0 0;
      }
    }
  }
}
.show {
  display: block;
}
</style>
