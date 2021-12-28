<template>
  <view class="water-conservation">
    <view class="above">
      根据《江苏省节约⽤⽔条例》《江苏省节⽔⾏动实施⽅案》和省⽔利厅、省发展改
      ⾰委《关于进⼀步规范省级节⽔型载体管理的通知》（苏⽔节〔2020〕8 号）要求，各地应积极
      开展省级节⽔型企业、社区、灌区等载体建设
    </view>
    <view class="item">
      <view class="left">
        <text>查询管理规范</text>
      </view>
      <view class="right">
        <text>江苏省水利厅文件</text>
        <u-icon name="arrow-right" color="#9ba0ab" size="12"/>
      </view>
    </view>
    <view class="table-box">
      <view class="title">文件及归档材料</view>
      <view class="table">
        <view class="roll">
          <view class="head">
            <text class="number">#</text>
            <text class="type">申报年度</text>
            <text class="yield">任务下达文件</text>
            <text class="opinion">创建成功文件</text>
            <text class="report">台账资料</text>
            <text class="report">复查情况</text>
          </view>
          <view class="body-r">
            <text class="number">01</text>
            <text class="type">2021</text>
            <text class="yield">任务文件.txt</text>
            <text class="opinion">成功文件.txt</text>
            <text class="report">台账</text>
            <text class="report">情况描述</text>
          </view>
          <view class="body-r">
            <text class="number">02</text>
            <text class="type">2021</text>
            <text class="yield">任务文件.txt</text>
            <text class="opinion">成功文件.txt</text>
            <text class="report">台账</text>
            <text class="report">情况描述</text>
          </view>
          <view class="body-r">
            <text class="number">03</text>
            <text class="type">2021</text>
            <text class="yield">任务文件.txt</text>
            <text class="opinion">成功文件.txt</text>
            <text class="report">台账</text>
            <text class="report">情况描述</text>
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
.water-conservation{
  .above{
    padding: 28rpx 32rpx 18rpx;
    font-size: 28rpx;
    font-family: PingFangSC, PingFangSC-Regular;
    font-weight: 400;
    color: #262626;
    line-height: 48rpx;
    border-bottom: 20rpx solid #f7f7f7;
  }
  .item {
    border-bottom: 2rpx solid #e6e6e6;
    background-color: #ffffff;
    height: 100rpx;
    line-height: 100rpx;
    padding: 0 24rpx 0 32rpx;
    display: flex;
    justify-content: space-between;

    .left {
      font-size: 28rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #333333;
    }

    .right {
      display: flex;
      font-size: 26rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #1471FF;

      text {
        padding-right: 18rpx;
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
      overflow-x: auto;
      border: 2rpx solid #e6e6e6;
      width: 696rpx;
      margin: 0 auto;
      .roll{
        width: 780rpx;
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
            flex: 3;
          }
          .opinion{
            flex: 3;
          }
          .report{
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
            flex: 2;
          }
          .yield{
            flex: 3;
          }
          .opinion{
            flex: 3;
          }
          .report{
            flex: 2;
          }
        }
        .body-r:nth-child(2n + 1){
          background: #f7f7f7;
        }
      }
    }
  }
}
</style>
