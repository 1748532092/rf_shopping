
<template name="product_details">
  <view class="product_details">
    <navigator
      class="back_btn icon iconfont"
      url="/pages/home_page/home_page"
      open-type="navigateBack"
      delta="1"
      hover-class="none"
      >&#xe628;</navigator
    >
    <view class="product_img">
      <swiper>
        <swiper-item class="swiper_item">
          <image src="../static/goods.jpg"></image>
          <view class="tag"> 1/1 </view>
        </swiper-item>
      </swiper>
    </view>
    <!-- 商品信息 -->
    <view class="product_information">
      <view class="introduce_first_line">
        <view>
          <text class="product_price">该商品仅需10000积分</text>
        </view>
        <view class="collect">
          <view class="icon iconfont">&#xe60a;</view>
          <text>收藏</text>
        </view>
      </view>
      <view class="introduce_second_line">
        <view class="title">
          <text
            >狗狗零食牛肉粒补钙除口臭训狗奖励泰迪金毛幼犬小狗零食宠物用品</text
          >
        </view>
        <view class="share">
          <text class="icon iconfont">&#xe658;</text>
          <text>分享</text>
        </view>
      </view>
      <view class="product_tag">
        <button class="product_poster">生成海报</button>
      </view>
      <view class="product_data">
        <text class="item">快递：包邮</text>
        <text class="item">月销 882</text>
        <text class="item">上海市 市辖区 黄浦区</text>
      </view>
    </view>
    <!-- 商品库存、购买类型等 -->
    <view class="product_list">
      <view class="goods_stock">
        <view class="item">
          <view class="left">
            <text class="title">商品库存</text>
          </view>
          <view class="middle">
            <text class="content">600kg</text>
          </view>
        </view>
        <view class="item">
          <view class="left">
            <text class="title">购买类型</text>
          </view>
          <view class="middle">
            <text class="content">请选择规格</text>
          </view>
          <view class="right">
            <text class="icon iconfont">&#xe62e;</text>
          </view>
        </view>
        <view class="item">
          <view class="left">
            <text class="title">积分活动</text>
          </view>
          <view class="middle">
            <text class="content">兑换类型：只支持积分兑换</text>
            <br />
            <!-- <text class="content">兑换所需积分：10000</text> -->
          </view>
        </view>
        <view class="item">
          <view class="left">
            <text class="title">服务</text>
          </view>
          <view class="middle">
            <text class="content">担保交易</text>
          </view>
          <view class="right">
            <text class="icon iconfont">&#xe62e;</text>
          </view>
        </view>
      </view>
    </view>
    <view class="product_evaluate">
      <view class="header">
        <text class="title">评价(2)</text>
        <text>好评率100.00%</text>
        <text class="icon iconfont">&#xe62e;</text>
      </view>
      <view class="content">
        <view>
          <image class="photo" src="../static/missing-face.png"></image>
        </view>
        <view class="right">
          <view class="name">
            <text>匿名用户</text>
          </view>
          <text class="eva_contente">123</text>
          <view class="buy_data">
            <text>购买类型：基础款</text>
            <text>2020-05-30 21:38</text>
          </view>
        </view>
      </view>
    </view>
    <view class="detail">
      <view class="title">
        <view class="line"></view>
        <text class="name">商品详情</text>
        <view class="line"></view>
      </view>
      <view class="content">
        <text
          >狗狗零食牛肉粒补钙除口臭训狗奖励泰迪金毛幼犬小狗零食宠物用品</text
        >
      </view>
      <image src="../static/goods.jpg"></image>
    </view>
    <view class="page_bottom">
      <view class="left">
        <navigator
          class="item"
          url="/pages/home_page/home_page"
          open-type="switchTab"
          hover-class="none"
        >
          <view class="icon iconfont">&#xe603;</view>
          <text>首页</text>
        </navigator>
        <navigator
          class="item"
          url="/pages/cart/cart"
          open-type="switchTab"
          hover-class="none"
        >
          <view class="icon iconfont">&#xe605;</view>
          <text>购物车</text>
        </navigator>
        <view class="item">
          <view class="icon iconfont">&#xe709;</view>
          <text>客服</text>
        </view>
      </view>
      <view class="right">
        <button class="buy_now" @click="show = true">立即购买</button>
        <u-popup mode="bottom" v-model="show">
          <view class="content">
            <view class="product_inf">
              <image class="img" src="../static/goods.jpg"></image>
              <view class="pop_right">
                <view class="title item">狗狗零食</view>
                <view class="item price">该商品仅需10000积分</view>
                <view class="item">库存:94包</view>
              </view>
            </view>
            <view class="pur_num">
              <text>购买数量</text>
              <u-number-box v-model="value" @change="valChange"></u-number-box>
            </view>
            <view style="margin-top: 20rpx">
              <navigator class="ok_btn" @click="show = false" url="/pages/more_pages/create_order">完成</navigator>
            </view>
          </view>
        </u-popup>
        <button class="add_cart">加入购物车</button>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      value: 1,
    };
  },
  methods: {
    valChange(e) {
      console.log("当前值为: " + e.value);
    },
  },
};
</script>

<style lang="scss" scoped>
.product_details {
  background: #f8f8f8;
  .back_btn {
    font-size: 40rpx;
    position: fixed;
    padding-top: 100rpx;
    left: 40rpx;
    top: 40rpx;
    z-index: 3;
  }
  .product_img {
    height: 722rpx;
    position: relative;
    swiper {
      height: 100%;
    }
    .swiper_item {
      display: flex;
      justify-content: center;
      align-content: center;
      height: 750rpx;
      overflow: hidden;
      border-bottom: 1rpx solid rgba(0, 0, 0, 0.01);
      image {
        width: 100%;
        height: 100%;
      }
      .tag {
        background: #fa436a;
        color: #fff;
        position: absolute;
        bottom: 20rpx;
        right: 20rpx;
        font-size: 24rpx;
        border-radius: 2em;
        padding: 0 28rpx;
      }
    }
  }
  .product_information {
    font-size: 28rpx;
    background: #fff;
    padding-bottom: 20rpx;
    padding-left: 20rpx;
    .introduce_first_line {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20rpx 30rpx 10rpx;
      .product_price {
        padding: 10rpx 0;
      }
      .collect {
        width: 60rpx;
        text-align: center;
        font-size: 24rpx;
        color: #909399;
        .iconfont {
        }
        text {
          text-align: center;
        }
      }
    }
    .introduce_second_line {
      display: flex;
      justify-content: space-between;
      padding-left: 30rpx;
      align-items: center;
      padding-bottom: 10rpx;
      .title {
        font-size: 28rpx;
        color: #000;
      }
      .share {
        height: 60rpx;
        line-height: 60rpx;
        padding: 0 20rpx;
        font-size: 23rpx;
        width: 110rpx;
        margin-left: 20rpx;
        color: #fa436a;
        background: #f8f8f8;
        border-top-left-radius: 2em;
        border-bottom-left-radius: 2em;
        .iconfont {
          font-size: 22rpx;
          margin: 0 8rpx;
        }
      }
    }
    .product_tag {
      padding: 0 30rpx;
      margin: 10rpx 0;
      .product_poster {
        display: inline-flex;
        border-radius: 2em;
        height: 50rpx;
        line-height: 50rpx;
        background: #fa463a;
        color: #fff;
        font-size: 24rpx;
      }
    }
    .product_data {
      padding: 0 20rpx;
      display: flex;
      justify-content: space-between;
      .item {
        font-size: 24rpx;
        color: #909399;
      }
    }
  }
  .product_list {
    background: #fff;
    margin: 20rpx 0;
    .goods_stock {
      .item {
        display: flex;
        position: relative;
        border-bottom: 1rpx solid #f8f8f8;
        height: 80rpx;
        line-height: 80rpx;
        padding: 0 30rpx;
        .left {
          margin-right: 30rpx;
          .title {
            font-size: 28rpx;
          }
        }
        .middle {
          display: flex;
          .content {
            font-size: 26rpx;
            padding: auto;
            flex-direction: column;
            color: #303133;
          }
        }
        .iconfont {
          position: absolute;
          right: 30rpx;
        }
      }
    }
  }
  .product_evaluate {
    margin: 30rpx 0;
    background: #fff;
    display: flex;
    flex-direction: column;
    padding: 20rpx 30rpx;

    .header {
      display: flex;
      align-items: center;
      height: 70rpx;
      font-size: 28rpx;
      color: #909399;
      .title {
        flex: 1;
        font-size: 30rpx;
        color: #303133;
        margin-right: 4rpx;
      }
      .iconfont {
        margin-left: 10rpx;
      }
    }
    .content {
      display: flex;
      padding: 20rpx 0;
      .photo {
        width: 80rpx;
        height: 80rpx;
        border-radius: 100rpx;
      }
      .right {
        flex: 1;
        display: flex;
        flex-direction: column;
        color: #606266;
        padding-left: 26rpx;
        font-size: 28rpx;

        .eva_content {
          color: #303133;
        }
        .buy_data {
          display: flex;
          justify-content: space-between;
        }
      }
    }
  }
  .detail {
    margin: 30rpx 0 50rpx;
    background: #fff;
    .title {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 40rpx 20% 20rpx;
      .line {
        border-bottom: 1rpx solid rgba(0, 0, 0, 0.15);
        width: 120rpx;
      }
      .name {
        margin: 0 10rpx;
        font-size: 28rpx;
      }
    }
    .content {
      font-size: 28rpx;
    }
    image {
      max-width: 90%;
      display: inline-block;
      position: relative;
    }
  }
  .page_bottom {
    background: #fff;
    position: fixed;
    left: 0;
    bottom: 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10rpx 20rpx;
    .left {
      width: 300rpx;
      display: flex;
      align-items: center;
      margin-left: 10rpx;
      .item {
        flex: 1;
        font-size: 24rpx;
        color: #606266;
        text-align: center;
        .iconfont {
        }
      }
    }
    .right {
      display: flex;
      margin-left: 50rpx;
      .buy_now {
        font-size: 24rpx;
        background: #fa436a;
        color: #fff;
        border-top-left-radius: 2em;
        border-bottom-left-radius: 2em;
      }
      .content {
        padding: 24rpx;
        font-size: 28rpx;
        .product_inf {
          display: flex;
          border-bottom: 1rpx solid #e7e2e2;
          .img {
            width: 250rpx;
            height: 150rpx;
          }
          .pop_right {
            text-align: left;
            .title {
              text-overflow: ellipsis;
              white-space: nowrap;
              overflow: hidden;
            }
            .item {
              margin: 10rpx;
            }
            .price {
              color: #fa436a;
            }
          }
        }
        .pur_num {
          margin-top: 20rpx;
          display: flex;
          justify-content: space-between;
          align-items: center;
        }
        .ok_btn {
          width: 90%;
          font-size: 30rpx;
          border-radius: 2em;
          height: 60rpx;
          line-height: 60rpx;
          background: #fa436a;
          color: #fff;
          margin-top: 40rpx;
          text-align: center;
          margin: 0 auto;
        }
      }
      .add_cart {
        font-size: 24rpx;
        border-top-right-radius: 2em;
        border-bottom-right-radius: 2em;
      }
    }
  }
}
</style>