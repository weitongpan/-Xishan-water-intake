<template>
	<view class="supervision-details">
    <u-toast ref="uToast"/>
    <view class="item-box border-b">
      <text class="left">监管内容</text>
      <text class="right">日常监管</text>
    </view>
    <view class="describe-box">
      <view class="describe">
        <view class="title">现场检查记录</view>
        <view class="text">
          <view class="file-text" @click="tips">文件材料6.pdf</view>
          <view class="file-text" @click="tips">文件材料4.pdf</view>
          <view class="file-text" @click="tips">现场图片.png</view>
          <view class="file-text" @click="tips">现场图片.jpg</view>
        </view>
      </view>
    </view>
    <view class="describe-box">
      <view class="describe">
        <view class="title">检查结果</view>
        <view class="text">
          这里是示例文字：根据《江苏省节约用水条例》《江苏省节水行动实施方案》和省水利厅、省发展改革委《关于进一步规范省级节水型载体管理的通知》
        </view>
      </view>
    </view>
    <view class="describe-box border-b rectification">
      <view class="describe">
        <view class="title">整改或处理</view>
        <view class="text">
          这里是示例文字：根据《江苏省节约用水条例》《江苏省节水行动实施方案》和省水利厅、省发展改革委《关于进一步规范省级节水型载体管理的通知》
        </view>
      </view>
    </view>
    <view class="item-box">
      <text class="left">填报单位</text>
      <text class="right">东港镇水利管理站</text>
    </view>
    <view class="item-box">
      <text class="left">填报人</text>
      <text class="right">刘娟</text>
    </view>
    <view class="item-box">
      <text class="left">填报日期</text>
      <text class="right">2021-11-25</text>
    </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
      tips() {
        this.$refs.uToast.show({
          message: '详情查阅锡山区取水监管信息化系统',
          duration: 2000
        })
      }
		}
	}
</script>

<style lang="scss">
.supervision-details{
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
      color: #333333;
    }
    .right{
      font-size: 26rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #808080;
    }
  }
  .border-b{
    border-bottom: 20rpx solid #f7f7f7;
  }
  .describe-box{
    .describe{
      width: 700rpx;
      margin: 0 auto;
      border-radius: 12rpx;
      .title{
        font-size: 28rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #333333;
        margin: 24rpx 0 28rpx;
      }
      .text{
        padding: 18rpx 14rpx 18rpx 28rpx;
        background: #f7f7f7;
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #808080;
        line-height: 44rpx;
        .file-text{
          color: #0f6eff;
          padding: 15rpx 0;
        }
      }
    }
  }
  .rectification{
    padding-bottom: 20rpx;
  }
}
</style>
