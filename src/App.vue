<!--
 * @Author: your name
 * @Date: 2021-04-15 14:23:42
 * @LastEditTime: 2021-04-28 18:00:45
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \TinyShop-UniApp-based:\Desktop\rf_shopping\src\App.vue
-->


<script>

export default {

  onLaunch: function () {
    console.log("App Launch");
  },
  onShow: function () {
    console.log("App Show");
  },
  onHide: function () {
    console.log("App Hide");
  },
};
</script>

<style lang="scss">
/*每个页面公共css */
@import './uview-ui/theme.scss';
@import "./static/css/iconfont/icon.css";
page{
  height: 100%;
  background: #f8f8f8;
}
</style>
