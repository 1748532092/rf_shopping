<!--
 * @Author: your name
 * @Date: 2021-04-12 15:44:29
 * @LastEditTime: 2021-04-15 17:42:26
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \rf-shopping\src\pages\classification\classification.vue
-->
<template>
   <view>
       <view>
           <view
        class="statusBar"
        :style="{ paddingTop: statusBarHeight + 'px' }"
      ></view>
        <view class="nav_title">分类</view>
       </view>
       <view class="search_row">
       <view class="sort_icon">
           <view class="icon iconfont">&#xe60e;</view>
       </view>
       <view class="search_box">
           <input placeholder="蔬菜"/>
           <view class="icon iconfont">&#xe647;</view>
       </view>
       </view>
   </view>
</template>

<script>
export default {
    date(){
        return{
             // 状态栏高度
      statusBarHeight: 0,
        }
    },
 //第一次加载时调用
  created() {
    //获取手机状态栏高度
    this.statusBarHeight = uni.getSystemInfoSync()["statusBarHeight"];
    console.log(this.statusBarHeight)
  },
}

</script>

<style lang="less" scoped>
.nav_title{
    font-size: 30RPX;
    text-align: center;
}
 .search_row{
    .sort_icon{

    }
 }
</style>