<!--
 * @Author: your name
 * @Date: 2021-04-12 15:45:00
 * @LastEditTime: 2021-04-14 10:10:49
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\user\user.vue
-->
<template>
<view>
    <view class="pure_top">
        <view class="person_information">
            <image class="photo_img" src="../../static/missing-face.png"></image>
            <text class="lod_text">登录/注册</text>
        </view>
    </view>
</view>
  
</template>

<script>
export default {

}
</script>

<style lang="less" scoped>
.pure_top {
 width: 100%;
  height: 150px;
  position: relative;
  z-index: -1;
  overflow: hidden;
}
.pure_top::after {
  content: '';
  width: 120%;
  height: 150px;
  position: absolute;
  left: -10%;     /* //椭圆左边隐藏10%，右边隐藏10% */
  top: 0;
  border-radius: 0 0 35% 35%; /*  //左上角，右上角，右下角，左下角 */
  background: url("../../static/user_bg.png");
}
.person_information{
    display: flex;
   
    .photo_img{
         z-index: 1;
        height: 100rpx;
        width: 100rpx;
    }
}

</style>