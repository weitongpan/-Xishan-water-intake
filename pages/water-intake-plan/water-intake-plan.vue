<template>
	<view class="water-intake-plan">
    <view class="table-box">
      <view class="roll">
        <view class="table">
          <view class="head">
            <view class="number">
              <text>#</text>
            </view>
            <view class="year">
              <text>填报年度</text>
            </view>
            <view class="application">
              <text>年计划取水量</text>
            </view>
            <view class="evaluation-form">
              <text>取水总结和计划申请表</text>
            </view>
            <view class="decision">
              <text>取水计划下达文件</text>
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
              <text>计划表.txt</text>
            </view>
            <view class="evaluation-form">
              <text>申请表.txt</text>
            </view>
            <view class="decision">
              <text>文件.txt</text>
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
              <text>计划表.txt</text>
            </view>
            <view class="evaluation-form">
              <text>申请表.txt</text>
            </view>
            <view class="decision">
              <text>文件.txt</text>
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
              <text>计划表.txt</text>
            </view>
            <view class="evaluation-form">
              <text>申请表.txt</text>
            </view>
            <view class="decision">
              <text>文件.txt</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>999</text>
            </view>
            <view class="year">
              <text>2021</text>
            </view>
            <view class="application">
              <text>计划表.txt</text>
            </view>
            <view class="evaluation-form">
              <text>申请表.txt</text>
            </view>
            <view class="decision">
              <text>文件.txt</text>
            </view>
          </view>
        </view>
      </view>
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

		}
	}
</script>

<style lang="scss">
.water-intake-plan{
  .table-box{
    padding: 24rpx 30rpx;
    .roll{
      overflow-x: auto;
      .table{
        width: 880rpx;
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
            flex: 2;
            text-align: center;
          }
          .year{
            flex: 4;
          }
          .application{
            flex: 5;
          }
          .evaluation-form{
            flex: 8;
          }
          .decision{
            flex: 6;
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
            flex: 2;
            text-align: center;
          }
          .year{
            flex: 4;
          }
          .application{
            flex: 5;
          }
          .evaluation-form{
            flex: 8;
          }
          .decision{
            flex: 6;
          }
        }
        .table-r:nth-child(2n + 1) {
          background: #f7f7f7;
        }
      }
    }

  }
}
</style>
