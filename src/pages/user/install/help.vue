<!--
 * @Author: your name
 * @Date: 2021-04-20 15:33:18
 * @LastEditTime: 2021-04-23 18:06:55
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\pages\user\install\help.vue
-->
<template>
  <view class="help">
    <u-collapse :item-style="itemStyle">
      <u-collapse-item
        class="item"
        :title="item.head"
        v-for="(item, index) in itemList"
        :key="index"
      >
        <view class="item_content">
          {{ item.body }}
          <text class="icon iconfont">&#xe62e;</text>
        </view>
      </u-collapse-item>
    </u-collapse>
  </view>
</template>

<script>
export default {
  data() {
    return {
      itemList: [
        {
          head: "如何下载、安装、注册守候者",
          body: "下载",
          open: true,
        },
        {
          head: "帮不帮",
          body: "帮",
          open: true,
        },
      ],
      itemStyle: {
        background: "white",
        marginLeft: "50rpx",
        marginTop: "20rpx",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.help {
  padding-top: 20rpx;
  background: #f8f8f8;
  height: 100%;
  .item {
    .item_content {
    }
    .iconfont {
    }
  }
}
</style>