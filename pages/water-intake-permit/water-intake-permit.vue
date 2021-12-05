<template>
	<view class="water-intake-permit">
    <u-toast ref="uToast"/>
    <view class="item-box">
      <text class="left">单位名称</text>
      <text class="right">南国红豆控股有限公司</text>
    </view>
    <view class="item-box">
      <text class="left">取水许可证首页</text>
      <text class="right see" @click="open">查看大图</text>
    </view>
    <view class="item-box">
      <text class="left">起始日期</text>
      <text class="right">2021-07-07</text>
    </view>
    <view class="item-box">
      <text class="left">有效日期</text>
      <text class="right">2026-07-06</text>
    </view>
    <view class="item-box">
      <text class="left">水源类型</text>
      <text class="right">地表水</text>
    </view>
    <view class="item-box">
      <text class="left">年允许取水量(万m³/年)</text>
      <text class="right">200</text>
    </view>
    <view class="item-box">
      <text class="left">允许日最大取水量（m³/天）</text>
      <text class="right">5479.5</text>
    </view>
    <view class="item-box">
      <text class="left">允许最大取水流量（m³/秒）</text>
      <text class="right">0.063</text>
    </view>
    <view class="item-box">
      <text class="left">允许日最大取水量（m³/天）</text>
      <text class="right">5479.5</text>
    </view>
    <view class="item-box">
      <view>
        <text class="left">取水许可申请表</text>
      </view>
      <view class="right-box">
        <text class="right">2021-11-15</text>
        <u-icon name="arrow-right" size="16" color="#D5D5D5"></u-icon>
      </view>

    </view>
    <view class="item-box">
      <view>
        <text class="left">取水许可登记表</text>
      </view>
      <view class="right-box">
        <text class="right">2021-11-15</text>
        <u-icon name="arrow-right" size="16" color="#D5D5D5"></u-icon>
      </view>

    </view>
    <view class="item-box">
      <view>
        <text class="left">取水许可批复文件</text>
      </view>
      <view class="right-box">
        <text class="right">2021-11-15</text>
        <u-icon name="arrow-right" size="16" color="#D5D5D5"></u-icon>
      </view>

    </view>
    <view class="item-box">
      <text class="left">取水许可证</text>
      <text class="right"></text>
    </view>
    <view class="table-box">
      <view class="title">延续审批材料</view>
      <view class="roll">
        <view class="table">
          <view class="head">
            <view class="number">
              <text>#</text>
            </view>
            <view class="year">
              <text style="color: #FB1818">*</text>
              <text>年份</text>
            </view>
            <view class="application">
              <text>延续取水申请表</text>
            </view>
            <view class="evaluation-form">
              <text>延续取水评估表</text>
            </view>
            <view class="decision">
              <text>延续取水决定书</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>01</text>
            </view>
            <view class="year">
              <text>2021</text>
            </view>
            <view class="application">
              <text>延续取水申请表</text>
            </view>
            <view class="evaluation-form">
              <text>申请表1.txt</text>
            </view>
            <view class="decision">
              <text>决定书1.txt</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>02</text>
            </view>
            <view class="year">
              <text>2021</text>
            </view>
            <view class="application">
              <text>延续取水申请表</text>
            </view>
            <view class="evaluation-form">
              <text>申请表1.txt</text>
            </view>
            <view class="decision">
              <text>决定书1.txt</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>03</text>
            </view>
            <view class="year">
              <text>2021</text>
            </view>
            <view class="application">
              <text>延续取水申请表</text>
            </view>
            <view class="evaluation-form">
              <text>申请表1.txt</text>
            </view>
            <view class="decision">
              <text>决定书1.txt</text>
            </view>
          </view>
        </view>
      </view>
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
    onLoad() {
      this.$refs.uToast.show({
        message: '详情查阅锡山区取水监管信息化系统',
        duration: 2000
      })
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
.water-intake-permit{
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
    .right-box{
      display: flex;
      .right{
        padding-right: 14rpx;
      }
    }
  }
  .table-box{
    padding: 24rpx 30rpx;
    .title{
      font-size: 28rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #808080;
      margin-bottom: 20rpx;
    }
    .roll{
      overflow-x: auto;
      .table{
        width: 850rpx;
        border: 2rpx solid #e6e6e6;
        .head{
          display: flex;
          font-size: 24rpx;
          color: #333333;
          font-family: PingFangSC, PingFangSC-Regular;
          font-weight: 400;
          height: 72rpx;
          line-height: 72rpx;
          background: #f1f6ff;
          .number{
            flex: 4;
            text-align: center;
          }
          .year{
            flex: 6;
          }
          .application, .evaluation-form, .decision{
            flex: 10;
          }
        }
        .table-r{
          display: flex;
          font-size: 24rpx;
          color: #808080;
          font-family: PingFangSC, PingFangSC-Regular;
          font-weight: 400;
          height: 72rpx;
          line-height: 72rpx;
          .number{
            flex: 4;
            text-align: center;
          }
          .year{
            flex: 6;
          }
          .application, .evaluation-form, .decision{
            flex: 10;
          }
        }
        .table-r:nth-child(2n + 1) {
          background: #f7f7f7;
        }
      }
    }

  }
  .popup-img-box{
    image{
      width: 700rpx;
      height: 524rpx;
    }
  }
}
</style>
