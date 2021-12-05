<template>
  <view class="audit">
    <view class="above">
      根据《江苏省节约用水条例》第十三条的规定： 计划用水户应当加强用水、节水设施的日常维护，建立用水、节水记录台账，定期进行用水合理性分析、水平衡测试，按时报送用水、节水报表。 重点计划用水户应当每三年开展一次水平衡测试，其他计划用水户应当每五年开展一次水平衡测试。计划用水户超计划用水百分之三十以上的，应当进行水平衡测试和接受水行政主管部门的用水审计，并对存在问题予以整改。
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
        <view class="head">
          <text class="number">#</text>
          <text class="type">归档年度</text>
          <text class="yield">用水审计报告</text>
          <text class="opinion">整改意见</text>
          <text class="report">企业整改报告</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">2021</text>
          <text class="yield">审计报告.txt</text>
          <text class="opinion">修改.txt</text>
          <text class="report">报告1.txt</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">2021</text>
          <text class="yield">审计报告.txt</text>
          <text class="opinion">修改.txt</text>
          <text class="report">报告1.txt</text>
        </view>
        <view class="body-r">
          <text class="number">01</text>
          <text class="type">2021</text>
          <text class="yield">审计报告.txt</text>
          <text class="opinion">修改.txt</text>
          <text class="report">报告1.txt</text>
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
.audit{
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
          flex: 2;
        }
        .yield{
          flex: 3;
        }
        .opinion{
          flex: 2;
        }
        .report{
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
          flex: 2;
        }
        .report{
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
