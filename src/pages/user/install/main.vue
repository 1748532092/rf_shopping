<template>
  <view class="install_page">
    <navigator class="list_item" v-for="(item,index) in list" :key="index" :url="item.url" >
    
        <text class="item_title">{{item.name}}</text>
      <text class="item_tip"></text>
      <text class="icon iconfont">&#xe62e;</text>
    
    </navigator>
    <view class="choose_color">
      <view class="item">
        <view class="content">
          <text class="icon iconfont">&#xe644;</text>
          <view class="color"></view>
          <view class="title"
            >主题色：
            <text style="color: #fa436a">官方</text>
          </view>
        </view>
        <view>
          <button class="choose_btn">
            <text class="icon iconfont">&#xe644;</text>
            <text>选择主题</text>
          </button>
        </view>
      </view>
    </view>
    <view class="log_out">
      <view class="btn_text">
		<u-modal  :show-title="false"  :show-cancel-button="true" v-model="show" :content="content" ></u-modal>
		<u-button  @click="open">
			退出登录
		</u-button>
	</view>
    </view>
  </view>
</template>
<script>
export default {
  data(){
    return{
      show: false,
				content: '确定要退出登录？', 
      //  "修改密码","授权管理","发票管理","开票历史","清楚缓存","关于商城","站点帮助","意见反馈"
      list:[
        {
          name: "个人资料",
          url: "/pages/user/install/personal_data"
          },
            {
          name: "修改密码",
          url: "/pages/user/install/change_password"
          },
            {
          name: "授权管理",
          url: "/pages/user/install/authorization_management"
          },
            {
          name: "发票管理",
          url: "/pages/user/install/invoices"
          },
            {
          name: "开票历史",
          url: "/pages/user/install/billing"
          },
            {
          name: "清理缓存",
          url: ""
          },
            {
          name: "关于商城",
          url: "/pages/user/install/about"
          },
            {
          name: "站点帮助",
          url: "/pages/user/install/help"
          },
            {
          name: "意见反馈",
          url: "/pages/user/install/feedback"
          },
        ]
    }
  },
  methods: {
			open() {
				this.show = true;
			}
		}
};
</script>
<style lang="scss" scoped>
.install_page {
  background: #f8f8f8;
  padding: 20rpx 0;
  .m_t {
    margin-top: 20rpx;
  }
  .list_item {
    display: flex;
    height: 60rpx;
    line-height: 60rpx;
    padding: 20rpx 30rpx;
    position: relative;
    background: #fff;
    justify-content: center;
    border-bottom: 1px solid #e4e7ed;
    &:nth-child(3n){
      margin-bottom: 20rpx;
    }
    .item_title {
      flex: 1;
      font-size: 30rpx;
      margin-left: 10rpx;
    }
    .item_tip {
      font-size: 28rpx;
      color: #909399;
    }
    .iconfont {
      color: #909399;
      margin-left: 10rpx;
    }
  }
  .choose_color {
    display: block;
    overflow: hidden;
   
    border-radius: 20rpx;
    width: 100vw;
    .item {
      position: relative;
      display: flex;
      padding: 0 30rpx;
      min-height: 100rpx;
      background-color: #ffffff;
      justify-content: space-between;
      align-items: center;
      .content {
        display: flex;
        font-size: 30rpx;
        align-items: center;
        .iconfont {
          color: #fa436a;
          display: inline-block;
          margin-right: 20rpx;
         
          text-align: center;
        }
        .color {
          background-color: #fa436a;
          width: 50rpx;
          height: 50rpx;
          border-radius: 6rpx;
          margin-right: 20rpx;
        }
        .title {
          font-size: 28rpx;
        }
      }
      .choose_btn {
        border-radius: 2em;
        position: relative;
        border: 0rpx;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        padding: 0 30rpx;
        font-size: 28rpx;
        height: 64rpx;
        line-height: 1;
        text-align: center;
        text-decoration: none;
        background-color: #fa436a;
        color: #fff;
        .iconfont{
            color: #fff;
            font-size: 28rpx;
        }
      }
    }
  }
  .log_out{
      display: flex;
      padding: 20rpx 30rpx;
      position: relative;
      background: #fff;
      justify-content: center;
      margin: 40rpx 0;
      .btn_text{
          flex: 1;
          font-size: 30rpx;
          color: #fa436a;
          text-align: center;
      }
  }
}
</style>