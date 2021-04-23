
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
      <u-notice-bar class="content" mode="vertical" :volume-icon="false" :list="list"></u-notice-bar>
        <view class="icon iconfont">&#xe62e;</view>
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
      <view class="new_products_content">
        <view class="goods_item" v-for="items in 4" :key="items">
          <view class="show_img">
            <image class="goods_img" src="../static/goods.jpg"></image>
            <image class="goods_label" src="../static/pinkage.png"></image>
          </view>
          <view class="goods_name"
            >狗狗零食牛肉粒补钙除口臭训狗奖励小泰迪金毛幼犬小狗狗</view
          >
          <view>
            <view class="selling_price">
              <view class="selling_price_sign">¥</view>
              <view class="selling_price_text">38</view>
            </view>
            <view class="original_price">
                <view class="original_price_sign">¥</view>
               <view class="original_price_text">45</view>
            </view>
          </view>
          <view class="goods_sales">
            <view style="display:inline">
              <span>301</span>
              <view class="sales_number">人付款</view>
              </view>
            <view class="icon iconfont">&#xe602; </view>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>
    
<script>
export default {
  name: "homeTab",
  data(){
    return{
        list:[
        123,
        456,
        789,
      ],
    }
  }
};
</script>

<style lang="scss" scoped>
.banner {
  display: flex;
  width: 640rpx;
  height: 300rpx;
  margin: auto;
  overflow: hidden;
  border-radius: 15rpx;
  position: relative;
  .banner_img {
    width: 100%;
    height: 100%;
  }
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
  width: 100%;
  display: flex;
  margin: 20rpx auto;
  .content{
    width: 100%;
  }
  .notice_icon {
    .iconfont {
      font-size: 50rpx;
      margin-left: 40rpx ;
     position: relative;
      line-height: 80rpx;
      color: red;
    }
  }
      .iconfont {
        position: absolute;
        right: 10rpx;
        display: inline;
        font-size: 50rpx;
        color: rgb(114, 106, 106);
      }
    
  }

.show {
  display: flex;
  margin: 0 auto;
  .bargain_img {
    height: 350rpx;
    width: 300rpx;
    margin:0 20rpx 0 30rpx;
  }
  .group_img {
    height: 170rpx;
    width: 370rpx;
  }
  .discount_img {
    height: 170rpx;
    width: 370rpx;
  }
}
.bargain_img {
  height: 400rpx;
  width: 320rpx;
}
.active_img {
  height: 200rpx;
  width: 690rpx;
  margin: 20rpx 30rpx;
}
.new_products_modules {
  .new_products_top {
    display: flex;
    position: relative;
    border-bottom:1rpx solid rgb(206, 194, 194);
    padding-bottom: 20rpx;
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
        line-height: 64rpx;
      }
    }
  }
  .new_products_content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    .goods_item {
      margin-top: 30rpx;
      .show_img {
        display: flex;
        height: 300rpx;
        width: 300rpx;
        position: relative;
        .goods_img {
          height: 300rpx;
          width: 300rpx;
          margin: auto;
        }
        .goods_label {
          height: 50rpx;
          width: 50rpx;
          position: absolute;
          top: 0;
          left: 0;
        }
      }
      .goods_name {
        height: 50rpx;
        width: 300rpx;
        font-size: 28rpx;
        overflow: hidden;
        text-overflow: ellipsis; //当对象内文本溢出时显示省略标记
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
        padding: 20rpx;
      }
      .selling_price{
        display: inline-flex;
        margin-right: 10rpx;
        .selling_price_sign{
          display: inline;
          font-size: 32rpx;
          color: red;
        }
        .selling_price_text{
          display: inline;
          font-size: 30rpx;
          color: red;
        }
      }
      .original_price{
        display: inline-flex;
        text-decoration: line-through;
        .original_price_sign{
          display: inline;
          font-size: 28rpx;
          color: rgb(124, 112, 112);
        }
        .original_price_text{
          display: inline;
          font-size: 26rpx;
          color: rgb(124, 112, 112);
          margin-left: 10rpx;
        }
      }
      .goods_sales{
        position: relative;
        width: 300rpx;
        padding: auto 20rpx;
        span{
            color: red;
             font-size: 26rpx;
          }
        .sales_number{
          display: inline;
          font-size: 26rpx;
        }
        .iconfont{
          position: absolute;
          right: 0;
          display: inline;
          font-size: 50rpx;
          color: red;
        }
      }
    }

  }
}
</style>