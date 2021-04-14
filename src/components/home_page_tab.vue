<!--
 * @Author: your name
 * @Date: 2021-04-14 09:03:28
 * @LastEditTime: 2021-04-14 17:43:52
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\components\home_page_tab.vue
-->
<template>
  <view>
    <!-- banner -->
    <view>
      <swiper class="banner" autoplay="true">
        <swiper-item style="height: 350rpx">
          <image class="banner_img" src="../static/two.jpg"></image>
          <!-- <view class="banner_text">1/2新鲜蔬菜</view> -->
        </swiper-item>
        <swiper-item>
          <image class="banner_img" src="../static/one.jpg"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="classify_row">
      <view style="display: inline">
        <image class="classify_img" src="../static/kj.png"></image>
        <view class="classify_text">家用电器</view>
      </view>
      <view style="display: inline">
        <image class="classify_img" src="../static/kj.png"></image>
        <view class="classify_text">男装</view>
      </view>
      <view style="display: inline">
        <image class="classify_img" src="../static/kj.png"></image>
        <view class="classify_text">手机</view>
      </view>
    </view>
    <view class="notice">
      <!-- 公告图片 -->
      <view class="notice_icon">
        <view class="icon iconfont">&#xe619;</view>
      </view>
      <!-- 公告内容 -->
      <view class="notice_text">
        <ul>
          <li>
            123
            <view class="icon iconfont">&#xe62e;</view>
          </li>
          <li>
            456
            <view class="icon iconfont">&#xe62e;</view>
          </li>
          <li>
            789
            <view class="icon iconfont">&#xe62e;</view>
          </li>
        </ul>
      </view>
    </view>
    <!-- 活动展示区 -->
    <view class="show">
      <view>
        <image class="bargain_img" src="../static/kj.png"></image>
      </view>
      <view>
        <view>
          <image class="group_img" src="../static/tg.png"></image>
        </view>
        <view>
          <image class="discount_img" src="../static/zk.png"></image>
        </view>
      </view>
    </view>
    <view>
      <image class="active_img" src="../static/share/banner_one.png"></image>
    </view>
    <!-- 新品上市 -->
    <view class="new_products_modules">
      <view class="new_products_top">
        <view class="icon iconfont">&#xe601;</view>
        <view class="new_products_top_right">
          <view>
            <view class="new_products_chinese">新品上市</view>
            <view class="new_products_english">New Products Listed</view>
          </view>

          <view class="icon iconfont">&#xe62e;</view>
        </view>
      </view>
    </view>
  </view>
</template>
    
<script>
export default {
  name: "homeTab",
};
</script>

<style lang="less" scoped>
.banner {
  display: flex;
  width: 90%;
  height: 200px;
  margin: 20rpx auto;
  overflow: hidden;
  border-radius: 15rpx;
  position: relative;
  .banner_img {
    width: 100%;
    height: 100%;
  }
  // .banner_text{
  //   position: absolute;
  //   bottom: 0;
  //   display: inline-flex;
  //   font-size: 34rpx;
  //  color: black;
  //   opacity: 0.5;
  // }
}
.classify_row {
  display: flex;
  justify-content: space-around;
  margin-top: 40rpx;
  .classify_img {
    width: 100rpx;
    height: 100rpx;
    border-radius: 50%;
  }
  .classify_text {
    font-size: 20rpx;
    text-align: center;
  }
}
div,
ul,
li {
  margin: 0;
  padding: 0;
} /*先初始化一下默认样式*/
.notice {
  display: flex;
  margin: 20rpx auto;
  .notice_icon {
    .iconfont {
      font-size: 50rpx;
      margin: auto 40rpx;
      line-height: 80rpx;
      color: red;
    }
  }
  .notice_text {
    display: flex;
    width: 600rpx; /*单行显示，超出隐藏*/
    height: 80rpx; /*固定公告栏显示区域的高度*/
    overflow: hidden;
    position: relative;
    li {
      list-style: none;
      line-height: 80rpx;
      font-size: 26rpx;
      /*以下为了单行显示，超出隐藏*/
      display: block;
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
      .iconfont {
        position: absolute;
        right: 0;
        display: inline;
        font-size: 50rpx;
        color: rgb(114, 106, 106);
      }
    }
  }
}
.show {
  display: flex;
  width: 90%;
  margin: 0 auto;
  .bargain_img {
    height: 420rpx;
    width: 320rpx;
    margin-right: 20rpx;
  }
  .group_img {
    height: 200rpx;
    width: 320rpx;
  }
  .discount_img {
    height: 200rpx;
    width: 320rpx;
  }
}
.bargain_img {
  height: 400rpx;
  width: 320rpx;
}
.active_img {
  height: 200rpx;
  width: 660rpx;
  margin: 20rpx 30rpx;
}
.new_products_modules {
  .new_products_top {
    display: flex;
    position: relative;
    .iconfont {
      margin: auto 30rpx;
      color: rgb(241, 70, 176);
      font-size: 50rpx;
    }
    .new_products_top_right {
      display: flex;
      .new_products_chinese {
        font-size: 32rpx;
      }
      .new_products_english {
        font-size: 26rpx;
        color: rgb(153, 144, 144);
      }
      .iconfont {
        display: inline;
        color: rgb(153, 144, 144);
        position: absolute;
        right: 0;
      }
    }
  }
}
</style>