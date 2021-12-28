<template>
	<view class="monitor">
    <view class="item-box">
      <text class="left">取水口</text>
      <text class="right">68</text>
    </view>
    <view class="item-box">
      <text class="left">取水口经度</text>
      <text class="right">1</text>
    </view>
    <view class="item-box">
      <text class="left">取水口纬度</text>
      <text class="right">1</text>
    </view>
    <view class="item-box">
      <text class="left">取水地点</text>
      <text class="right">锡山市东港镇红豆工业园区</text>
    </view>
    <view class="item-box">
      <text class="left">取水口远景图</text>
      <text class="right see" @click="open">查看大图</text>
    </view>
    <view class="item-box">
      <text class="left">取水口特写图</text>
      <text class="right see" @click="open">查看大图</text>
    </view>
    <view class="item-box">
      <text class="left">水资源分区</text>
      <text class="right">1</text>
    </view>

<!--    地表水显示内容-->
<!--    <view>-->
<!--      <view class="item-box">-->
<!--        <text class="left">水源类型</text>-->
<!--        <text class="right">地表水</text>-->
<!--      </view>-->
<!--      <view class="item-box">-->
<!--        <text class="left">取水设施类型</text>-->
<!--        <text class="right">水泵</text>-->
<!--      </view>-->
<!--      <view class="item-box">-->
<!--        <text class="left">水泵设计扬程（单位m)</text>-->
<!--        <text class="right">0.063</text>-->
<!--      </view>-->
<!--    </view>-->

<!--    地下水显示内容-->
    <view>
      <view class="item-box">
        <text class="left">水源类型</text>
        <text class="right">地下水</text>
      </view>
      <view class="item-box">
        <text class="left">取水设施类型</text>
        <text class="right">水井</text>
      </view>
      <view class="item-box">
        <text class="left">水井数量</text>
        <text class="right">2</text>
      </view>
      <view class="well">
        <view class="title">水井</view>
        <view class="table">
          <view class="head">
            <text class="number">#</text>
            <text class="type">开采层位</text>
            <text class="yield">井深(m)</text>
            <text class="quota">井径(m)</text>
          </view>
          <view class="body-r">
            <text class="number">01</text>
            <text class="type">第2层</text>
            <text class="yield">16</text>
            <text class="quota">2</text>
          </view>
          <view class="body-r">
            <text class="number">02</text>
            <text class="type">第2层</text>
            <text class="yield">16</text>
            <text class="quota">2</text>
          </view>
          <view class="body-r">
            <text class="number">03</text>
            <text class="type">第2层</text>
            <text class="yield">16</text>
            <text class="quota">2</text>
          </view>
        </view>
      </view>
    </view>


    <view class="item-box">
      <text class="left">日最大取水能力（单位m3/d)</text>
      <text class="right">5479.5</text>
    </view>
    <view class="item-box">
      <text class="left">取水工程（设施）验收申请书</text>
      <u-icon name="arrow-right" color="#e6e6e6" size="16"></u-icon>
    </view>
    <view class="item-box">
      <text class="left">取水工程（设施）验收报告</text>
      <u-icon name="arrow-right" color="#e6e6e6" size="16"></u-icon>
    </view>
    <view class="item-box">
      <text class="left">计量设备类型</text>
      <text class="right">水表</text>
    </view>
    <view class="item-box">
      <text class="left">计量内容</text>
      <text class="right">流量</text>
    </view>
    <view class="item-box">
      <text class="left">计量方式</text>
      <text class="right">管道计量</text>
    </view>
    <view class="item-box">
      <text class="left">数据传输方式</text>
      <text class="right">在线</text>
    </view>
    <view class="item-box">
      <text class="left">计量设施检验合格日期</text>
      <text class="right">2021-10-01</text>
    </view>
    <view class="item-box">
      <text class="left">检定校准要求</text>
      <text class="right">1</text>
    </view>
    <view class="item-box">
      <text class="left">计量设施远景图</text>
      <text class="right see" @click="open">查看大图</text>
    </view>
    <view class="item-box">
      <text class="left">计量设施特写图</text>
      <text class="right see" @click="open">查看大图</text>
    </view>
    <view class="item-box">
      <text class="left">计量率定报告</text>
      <u-icon name="arrow-right" color="#e6e6e6" size="16"></u-icon>
    </view>
    <view class="item-box">
      <text class="left">计量设施检验报告</text>
      <u-icon name="arrow-right" color="#e6e6e6" size="16"></u-icon>
    </view>
    <view class="table-box">
      <view class="title">⽇常运维记录</view>
      <view class="table">
        <view class="head">
          <text class="number">#</text>
          <text class="type">计量及监控设施状态</text>
          <text class="yield">填报日期</text>
          <text class="quota">填报人</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">设施状态略</text>
          <text class="yield">2021/23/09</text>
          <text class="quota">孙小姐</text>
        </view>
        <view class="body-r">
          <text class="number">02</text>
          <text class="type">设施状态略</text>
          <text class="yield">2021/23/09</text>
          <text class="quota">孙小姐</text>
        </view>
        <view class="body-r">
          <text class="number">03</text>
          <text class="type">设施状态略</text>
          <text class="yield">2021/23/09</text>
          <text class="quota">孙小姐</text>
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
.monitor{
  padding-bottom: 30rpx;
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
  .well{
    padding: 0 32rpx;
    .title{
      font-size: 28rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #808080;
      padding:26rpx 0 20rpx 0;
    }
    .table{
      border: 2rpx solid #e6e6e6;
      width: 696rpx;
      margin: 0 auto;
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
          flex: 1;
        }
        .yield{
          flex: 1;
        }
        .quota{
          flex: 1;
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
          color: #808080;
        }
        .number{
          flex: 1;
          text-align: center;
        }
        .type{
          flex: 1;
        }
        .yield{
          flex: 1;
        }
        .quota{
          flex: 1;
        }
      }
      .body-r:nth-child(2n + 1){
        background: #f7f7f7;
      }
    }
  }
  .table-box{
    padding: 0 32rpx;
    .title{
      font-size: 28rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #808080;
      padding:26rpx 0 20rpx 0;
    }
    .table{
      border: 2rpx solid #e6e6e6;
      width: 696rpx;
      margin: 0 auto;
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
          flex: 3;
        }
        .yield{
          flex: 2;
        }
        .quota{
          flex: 2;
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
          color: #808080;
        }
        .number{
          flex: 1;
          text-align: center;
        }
        .type{
          flex: 3;
        }
        .yield{
          flex: 2;
        }
        .quota{
          flex: 2;
        }
      }
      .body-r:nth-child(2n + 1){
        background: #f7f7f7;
      }
    }
  }
}
</style>
