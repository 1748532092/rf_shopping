<!--
 * @Author: your name
 * @Date: 2021-04-12 15:44:29
 * @LastEditTime: 2021-04-23 16:50:56
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\classification\classification.vue
-->
<template>
  <view class="class_page">
    <view class="search_row">
      <view class="sort_icon">
        <view class="icon iconfont">&#xe61c;</view>
      </view>
      <view class="search_box">
        <input class="input_text" placeholder="蔬菜" />
        <view class="icon iconfont">&#xe647;</view>
      </view>
    </view>
    <view class="main">
      <scroll-view scroll-y class="left">
        <view
          :class="index === currentIndex ? 'active menu_item' : 'menu_item'"
          v-for="(item, index) in leftMenuList"
          :key="index"
          @click="handleItemTap"
          data-index="index"
        >
          {{ item }}
        </view>
      </scroll-view>
      <scroll-view scroll-y class="right">
        <view
          class="goods_group"
          v-for="(item1, index1) in rightConent"
          for-index="index1"
          for-item="item1"
        >
          <view class="goods_title">
            {{ item1.title }}
            <text class="icon iconfont">&#xe62e;</text>
          </view>

          <view class="goods_item">
            <view
              class="goods_content"
              v-for="(item2, index2) in '{{item1.children}}'"
              for-index="index2"
              for-item="item2"
              :key="id"
            >
              <image class="img" :src="item2.img"></image>
              <view class="goods_name">{{ item2.name }}</view>
            </view>
          </view>
        </view>
      </scroll-view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      leftMenuList: ["家用电器", "数码产品", "服饰鞋包"],
      rightConent: [
        {
          title: "手机",
          id: "1",
          children: [
            {
              id: "1",
              name: "华为",
              img: "../../static/errorImage.jpg",
            },
            {
              id: "2",
              name: "华为",
              img: "../../static/errorImage.jpg",
            },
            {
              id: "3",
              name: "华为",
              img: "../../static/errorImage.jpg",
            },
          ],
        },
        {
          title: "手表配饰",
          id: "2",
          children: [
            {
              id: "1",
              name: "华为",
              img: "../../static/image_1.jpg",
            },
          ],
        },
      ],
      // 左侧菜单被点击
      currentIndex: 0,
    };
  },
  methods:{
    
   
     handleItemTap(e) {
   /*
   1、获取被点击的标题身上的索引
   2、给data中的currentIndex赋值
   */ 
  // const {index}=e.currentTarget.dataset;
  // let rightConent = this.Cates[index].children;
  // this.setData({
  //   currentIndex :index,
  //   rightConent
  // })
  },
  }
 
};
</script>

<style lang="scss" scoped>
.class_page {
  height: 100%;
  font-size: 28rpx;
  .search_row {
    display: flex;
    margin: 10rpx 15rpx;
    .sort_icon {
      .iconfont {
        color: red;
        line-height: 60rpx;
      }
    }
    .search_box {
      background: #f5f5f5;
      display: flex;
      border-radius: 2em;
      width: 675rpx;
      height: 60rpx;
      margin-left: 10rpx;
      line-height: 60rpx;
      .input_text {
        height: 100%;
        width: 100%;
        font-size: 26rpx;
        color: #888;
        padding-left: 20rpx;
      }
      .iconfont {
        padding-right: 20rpx;
      }
    }
  }
  .main {
    height: calc(100vh - 79rpx);
    display: flex;
    .left {
      flex: 2;
      background: #f5f5f5;
      .menu_item {
        height: 80rpx;
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
    .active {
      color: #fa436a;
      background: #fff;
      font-weight: bold;
      border-left: 2rpx solid #fa436a;
    }
    .right {
      flex: 5;
      background: #fff;
      .goods_group {
        .goods_title {
          display: flex;
          padding: 0 20rpx;
          justify-content: space-between;
          .iconfont {
          }
        }
        .goods_item {
          display: flex;
          flex-wrap: wrap;
          margin: 20rpx 0 30rpx;
          .goods_content {
            width: 33.33%;
            text-align: center;
            .img {
              width: 50%;
              height: 100rpx;
            }
            .goods_name {
            }
          }
        }
      }
    }
  }
}
</style>