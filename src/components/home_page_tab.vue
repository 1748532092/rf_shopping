<template name="homeTab">
  <view>
    <!-- banner -->
    <view class="home_page_banner">
      <image class="banner_img" src="../../static/share/banner_one.png"></image>
      <image class="banner_img" src="../static/alipay.png"></image>
    </view>
    <input class="input" style="background:black"/>
  </view>
</template>
    
<script>
export default {};
</script>

<style lang="less" scoped>
.home_page_banner {
  .banner_img {
    height: 500rpx;
    width: 500rpx;
    border-radius: 2em;
  }
}
</style>