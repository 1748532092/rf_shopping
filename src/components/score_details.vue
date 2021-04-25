<!--
 * @Author: your name
 * @Date: 2021-04-23 10:23:49
 * @LastEditTime: 2021-04-23 14:13:09
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\components\score_details.vue
-->
<template name="score_details">
  <view class="score_details">
      <view class="tips_box">
          <text>提示：积分可用来兑换指定商品</text>
      </view>
      <view class="content">
           <text>没有更多了</text>
      </view>
  </view>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.score_details{
.tips_box{
    width: 90%;
    margin: 20rpx 5%;
    height: 60rpx;
    border-radius: 2em;
    background: #fff5e2;
    border: 1px solid #ffeac1;
    color: #c8a86b;
    text-align: center;
    text{
        font-size: 26rpx;
    }
}
.content{
    color: rgb(180, 172, 172);
    font-size: 28rpx;
    text-align: center;
    margin-top: 20rpx;
}
}
</style>