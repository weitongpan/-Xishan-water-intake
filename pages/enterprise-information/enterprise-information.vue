<template>
	<view class="enterprise-information">
    <view class="item-box">
      <text class="left">单位名称</text>
      <text class="right">南国红豆控股有限公司</text>
    </view>
    <view class="item-box">
      <text class="left">统一社会信用代码</text>
      <text class="right">9194583920028330589D</text>
    </view>
    <view class="item-box">
      <text class="left">营业执照</text>
      <text class="right see" @click="open">查看大图</text>
    </view>
    <view class="item-box">
      <text class="left">法定代表人</text>
      <text class="right">周明江</text>
    </view>
    <view class="item-box">
      <text class="left">所属镇/街道</text>
      <text class="right">东港镇</text>
    </view>
    <view class="item-box">
      <text class="left">住所（地址）</text>
      <text class="right">锡山市东港镇红豆工业园区</text>
    </view>
    <view class="item-box">
      <text class="left">行业类别</text>
      <text class="right">电力生产</text>
    </view>
    <view class="table-box">
      <view class="title">主要产品</view>
      <view class="table">
        <view class="head">
          <text class="number">#</text>
          <text class="type">产品种类</text>
          <text class="yield">年产量</text>
          <text class="quota">行业用水定额</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">电力生产</text>
          <text class="yield">19000000000Kwh</text>
          <text class="quota">1.85m3/Mwh</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">电力生产</text>
          <text class="yield">19000000000Kwh</text>
          <text class="quota">1.85m3/Mwh</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">电力生产</text>
          <text class="yield">19000000000Kwh</text>
          <text class="quota">1.85m3/Mwh</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">电力生产</text>
          <text class="yield">19000000000Kwh</text>
          <text class="quota">1.85m3/Mwh</text>
        </view>
      </view>
    </view>
    <view class="item-box">
      <text class="left">取水用途</text>
      <text class="right">工业用水</text>
    </view>
    <view class="item-box">
      <text class="left">单位荣誉</text>
      <text class="right">区节水型企业1、节水型企业2、节水型企业3</text>
    </view>
    <view class="item-box">
      <text class="left">水务经理</text>
      <text class="right">陈玲燕</text>
    </view>
    <view class="item-box">
      <text class="left">联系电话1</text>
      <text class="right">17082739018</text>
    </view>
    <view class="item-box">
      <text class="left">联系电话1</text>
      <text class="right">17082739018</text>
    </view>
    <u-popup :show="show"
             mode="center"
             @close="close"
             :closeOnClickOverlay="true"
    >
      <view class="popup-img-box">
        <image src="../../static/water-intake-archives/wt@2x.png"/>
      </view>
    </u-popup>
	</view>
</template>

<script>
	export default {
		data() {
			return {
        show: false
			}
		},
		methods: {
      open() {
        this.show = true
      },
      close() {
        this.show = false
      }
		}
	}
</script>

<style lang="scss">
.enterprise-information{
  .item-box{
    height: 92rpx;
    line-height: 92rpx;
    padding: 0 30rpx;
    border-bottom: 2rpx solid #e6e6e6;
    display: flex;
    justify-content: space-between;
    .left{
      font-size: 28rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #808080;
    }
    .right{
      font-size: 26rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #333333;
    }
    .see{
      color: #0065ff;
    }
  }
  .table-box{
    .title{
      font-size: 28rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #808080;
      padding:26rpx 0 20rpx 32rpx;
    }
    .table{
      padding: 0 32rpx;
      .head{
        display: flex;
        height: 72rpx;
        line-height: 72rpx;
        text{
          flex: 2;
          font-size: 24rpx;
          font-family: PingFangSC, PingFangSC-Regular;
          font-weight: 400;
          color: #333333;
          background-color: #f1f6ff;
        }
        .number{
          flex: 1;
          text-align: center;
        }
        .type{
          flex: 2;
        }
        .yield{
          flex: 4;
        }
        .quota{
          flex: 3;
        }
      }
      .body-r{
        display: flex;
        height: 72rpx;
        line-height: 72rpx;
        text{
          flex: 2;
          font-size: 24rpx;
          font-family: PingFangSC, PingFangSC-Regular;
          font-weight: 400;
          color: #333333;
        }
        .number{
          flex: 1;
          text-align: center;
        }
        .type{
          flex: 2;
        }
        .yield{
          flex: 4;
        }
        .quota{
          flex: 3;
        }
      }
      .body-r:nth-child(2n + 1){
        background: #f7f7f7;
      }
    }
  }
}
</style>
