<!--
 * @Author: your name
 * @Date: 2021-04-12 11:46:20
 * @LastEditTime: 2021-04-12 17:41:06
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\home_page\home_page.vue
-->

<template>
   <view>
	   <view class="home_page_top">
		      <!-- 状态栏占位 -->
     		<view class="statusBar":style="{ paddingTop: statusBarHeight + 'px' }"></view>
		   <view class="search_scan">
			   <view>
				   <input class="input_box"  placeholder="蔬菜"/>
				   <image class="search_img" src=""></image>
			   </view>
		   </view>
       </view>
   </view>
</template>

<script>
	export default {
 	data() {
      return {
        // 状态栏高度
        statusBarHeight: 0,
      };
    },
    //第一次加载时调用
    created() {
      //获取手机状态栏高度
      this.statusBarHeight = uni.getSystemInfoSync()['statusBarHeight'];
    },
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="less" scoped>
.home_page_top{
	
	background: #fa436a;
	height: 250rpx;
	.search_scan{
		display: flex;
		justify-content: space-around;
		border: 1rpx solid #000;
		height: 60rpx;
		width: 80%;
		margin-top: 10rpx;
		.input_box{
			flex: 1;
			background: #fff;
			height: 60rpx;
			width: 100%;
			border-radius: 2em;
	}
	}	
}

</style>
