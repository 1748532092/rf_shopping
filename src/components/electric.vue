<template name="electricTab">
<view>
     <view class="empty">
         <view class="icon iconfont">&#xe60e;</view>
         <span>暂无该分类产品</span>
     </view>
       <view class="emty_recommend">
        <span></span>
        <p>为您推荐</p>
    </view>

</view>
    
</template>
<script>
export default {
    
}
</script>
    <<style lang="less" scoped>
    .empty{
        
        background: #fff;
        height:500rpx;
        
        .iconfont{
            height: 500rpx;
            font-size: 200rpx;
            color: red;
             text-align:center;
           line-height:500rpx;
        }
    }
     .emty_recommend{
         position:relative;
         height:1.875rem;
         line-height: 1.875rem;
         margin:2.47rem auto;
         text-align: center;
         i{
            display:block;
            height:1px;
            background:#e1e1e1;
            position:absolute;
            top:0.9rem;
            width:100%;}
         p{
            display:inline-block;
            font-size: 28rpx;
            color:#c1c1c1;
            text-align: center;
            margin:0 auto;
            position:relative;
            z-index:2;
            }
     }

    </style>