<template>
	<view class="levy">
    <view class="item-box one"
          @click="pickerShow"
    >
      <view>
        <text class="left">当前年度</text>
      </view>
      <view class="right-box">
        <text class="right">2021</text>
        <u-icon name="arrow-right" size="16" color="#D5D5D5"></u-icon>
      </view>

    </view>
    <view class="item-box">
      <text class="left">取水权人</text>
      <text class="right">南国红豆控股有限公司</text>
    </view>
    <view class="item-box">
      <text class="left">取水许可证编号</text>
      <text class="right">9194583920028330589D</text>
    </view>
    <view class="item-box">
      <text class="left">许可证年取水量(万m3/年)</text>
      <text class="right">200</text>
    </view>
    <view class="item-box">
      <text class="left">水资源类型</text>
      <text class="right">地表水</text>
    </view>
    <view class="item-box one">
      <text class="left">当年计划取水量(万m3)</text>
      <text class="right">0</text>
    </view>
    <view class="controller">
      <view @click="activeClick(0)" :class="{active: activeIndex === 0}">
        <text>取水量填报</text>
      </view>
      <view  @click="activeClick(1)" :class="{active: activeIndex === 1}">
        <text>水资源费</text>
      </view>
      <view @click="activeClick(2)" :class="{active: activeIndex === 2}">
        <text>水利工程费</text>
      </view>
    </view>
    <view class="table-box table-box1" v-if="activeIndex === 0">
      <view class="roll">
        <view class="table">
          <view class="head">
            <view class="number">
              <text>取水缴费期间</text>
            </view>
            <view class="year">
              <text>上月抄表数</text>
            </view>
            <view class="application">
              <text>本月抄表数</text>
            </view>
            <view class="evaluation-form">
              <text>本月取水量</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>2月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>3月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>4月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
          </view>
        </view>
      </view>
    </view>
    <view class="table-box" v-if="activeIndex === 1">
      <view class="roll">
        <view class="table">
          <view class="head">
            <view class="number">
              <text>取水缴费期间</text>
            </view>
            <view class="year">
              <text>收费标准</text>
            </view>
            <view class="application">
              <text>本月应收费用</text>
            </view>
            <view class="evaluation-form">
              <text>本月实收费用</text>
            </view>
            <view class="decision">
              <text>累计应收费用</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
        </view>
      </view>
    </view>
    <view class="table-box" v-if="activeIndex === 2">
      <view class="roll">
        <view class="table">
          <view class="head">
            <view class="number">
              <text>取水缴费期间</text>
            </view>
            <view class="year">
              <text>收费标准</text>
            </view>
            <view class="application">
              <text>本月应收费用</text>
            </view>
            <view class="evaluation-form">
              <text>本月实收费用</text>
            </view>
            <view class="decision">
              <text>累计应收费用</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>1月</text>
            </view>
            <view class="year">
              <text>0.3</text>
            </view>
            <view class="application">
              <text>0.00</text>
            </view>
            <view class="evaluation-form">
              <text>0</text>
            </view>
            <view class="decision">
              <text>0.00</text>
            </view>
          </view>
        </view>
      </view>
    </view>
    <u-picker :show="show"
              :columns="columns"
              :defaultIndex="[2]"
              @cancel="pickerHied"
              title="年份"
              :closeOnClickOverlay="true"

    />
	</view>
</template>

<script>
	export default {
		data() {
			return {
        show: false,
        activeIndex: 1,
        columns: [
          ['2020', '2019', '2018', '2017', '2016']
        ]
			}
		},
		methods: {
      pickerHied() {
        console.log(123)
        this.show = false
      },
      pickerShow() {
        this.show = true
      },
      activeClick(index) {
        this.activeIndex = index
      }
		}
	}
</script>

<style lang="scss">
.levy{
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
  .one{
    border-bottom: 20rpx solid #f7f7f7;
  }
  .controller{
    display: flex;
    view{
      flex: 1;
      text-align: center;
      margin-top: 14rpx;
      text{
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #333333;
        display: inline-block;
        padding-bottom: 10rpx;
      }
    }
    .active{
      text{
        color: #0065ff;
        display: inline-block;
        border-bottom: 4rpx solid #0065ff;
        padding-bottom: 10rpx;
      }
    }
  }
  .table-box{
    padding: 24rpx 30rpx;
    .roll{
      overflow-x: auto;
      .table{
        width: 840rpx;
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
            flex: 1;
            padding-left: 28rpx;
          }
          .year{
            flex: 1;
          }
          .application{
            flex: 1;
          }
          .evaluation-form{
            flex: 1;
          }
          .decision{
            flex: 1;
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
            flex: 1;
            padding-left: 28rpx;
          }
          .year{
            flex: 1;
          }
          .application{
            flex: 1;
          }
          .evaluation-form{
            flex: 1;
          }
          .decision{
            flex: 1;
          }
        }
        .table-r:nth-child(2n + 1) {
          background: #f7f7f7;
        }
      }
    }

  }
  .table-box1{
    .roll{
      overflow: hidden;
      .table{
        width: 686rpx;
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
            flex: 1;
            padding-left: 28rpx;
          }
          .year{
            flex: 1;
          }
          .application{
            flex: 1;
          }
          .evaluation-form{
            flex: 1;
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
            flex: 1;
            padding-left: 28rpx;
          }
          .year{
            flex: 1;
          }
          .application{
            flex: 1;
          }
          .evaluation-form{
            flex: 1;
          }
          .decision{
            flex: 1;
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
