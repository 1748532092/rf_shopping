<!--
 * @Author: your name
 * @Date: 2021-04-26 09:15:33
 * @LastEditTime: 2021-04-27 15:28:59
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
        <navigator
          class="icon iconfont"
          url="/pages/home_page/home_page"
          open-type="navigateBack"
          hover-class="none"
          >&#xe61b;</navigator
        >
        <view class="search_box">
          <view class="search_img">
            <view class="icon iconfont">&#xe647;</view>
          </view>
          <input class="input_text" placeholder="请输入关键字" />
        </view>
      </view>
      <view class="filter_bar">
        <view>
          <u-dropdown>
            <u-dropdown-item v-model="value" title="综合" :options="options">
            </u-dropdown-item>
          </u-dropdown>
        </view>
        <view>销量</view>
        <view class="icon iconfont">&#xe624;</view>
        <view>
          <u-popup v-model="show" mode="right" width="90%">
            <view class="filter_content">
              <view class="price_range">
                <text class="title">价格区间</text>
                <text class="tip">请选择价格区间</text>
                <view class="input_box">
                  <input
                    class="input_content"
                    id="input1"
                    onchange="compare()"
                    placeholder="最低价"
                  />
                  <span style="margin-top: 60rpx">-</span>
                  <input
                    class="input_content"
                    id="input2"
                    onchange="compare()"
                    placeholder="最高价"
                  />
                </view>
              </view>
              <view class="sort">
                <text class="title">全部分类</text>
                <view class="content">
                  <text class="item">家用电器</text>
                  <text class="item">数码产品</text>
                  <text class="item">服饰鞋包</text>
                </view>
              </view>
              <view class="brand">
                <text class="title">品牌</text>
                <view class="content">
                  <text class="item">喜得龙</text>
                  <text class="item">美的</text>
                  <text class="item">苏泊尔</text>
                </view>
              </view>
              <view class="bottom_btn">
                <view class="reset"> 重置 </view>
                <view class="define"> 确定 </view>
              </view>
            </view>
          </u-popup>
          <view @click="show = true">筛选</view>
        </view>
      </view>
      <view class="screen">
        <text class="item">全部</text>
        <text class="item">新品</text>
        <text class="item">推荐</text>
        <text class="item">热门</text>
      </view>
    </view>
    <product_list></product_list>
  </view>
</template>

<script>
import product_list from "../../components/product_list"
export default {
  components:{
     product_list,
  },
  data() {
    return {
      // 状态栏高度
      statusBarHeight: 0,
      value: 1,
      show: false,
      options: [
        {
          label: "综合",
          value: 1,
        },
        {
          label: "价格升序",
          value: 2,
        },
        {
          label: "价格降序",
          value: 3,
        },
      ],
    };
  },
  methods: {},
  //第一次加载时调用
  created() {
    //获取手机状态栏高度
    this.statusBarHeight = uni.getSystemInfoSync()["statusBarHeight"];
  },
};
function compare() {
  // 获取输入框的值
  var input1 = document.getElementById("input1");
  var input2 = document.getElementById("input2");
  // 输入框的值转为Number类型
  var num1 = parseInt(input1.value);
  var num2 = parseInt(input2.value);
}
</script>

<style lang="scss" scoped>
.header {
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
  .filter_bar {
    display: flex;
    justify-content: space-around;
    font-size: 28rpx;
    color: #333;
    margin-top: 40rpx;
    .filter_content {
      padding: 170rpx 30rpx 30rpx;
      .title {
        font-size: 28rpx;
        font-weight: bold;
      }
      .price_range {
        .tip {
          margin-left: 280rpx;
          color: #fa436a;
        }
        .input_box {
          display: flex;
          .input_content {
            text-align: center;
            margin: 50rpx 20rpx;
            background: #f7f7f7;
          }
        }
      }

      .content {
        display: flex;
        margin: 50rpx 0;
        word-wrap: break-word;
        .item {
          flex: 1;
          border: 1rpx solid rgba(0, 0, 0, 0.12);
          margin: 20rpx;
          border-radius: 2em;
          padding: 10rpx 30rpx;
          text-align: center;
          font-size: 26rpx;
          width: 40%;
        }
      }
      .bottom_btn {
        display: flex;
        position: fixed;
        bottom: 30rpx;
        text-align: center;
        line-height: 60rpx;
        margin-left: 25rpx;
        .reset {
          width: 250rpx;
          height: 60rpx;
          border-radius: 2em;
          margin: 0 20rpx;
          border: 1rpx solid #fa436a;
          color: #fa436a;
        }
        .define {
          width: 250rpx;
          height: 60rpx;
          border-radius: 2em;
          margin: 0 20rpx;
          background: #fa436a;
          color: #fff;
        }
      }
    }
  }
  .screen {
        margin: 30rpx auto;
        display: flex;
        justify-content: center;
        .item {
          font-size: 28rpx;
          height: 40rpx;
          line-height: 40rpx;
          padding: 10rpx 40rpx;
          margin: 0 20rpx;
          border-radius: 2em;
          border: 1rpx solid rgba(0, 0, 0, 0.12);
        }
      }
}
</style>