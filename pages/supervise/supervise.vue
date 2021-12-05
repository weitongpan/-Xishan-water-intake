<template>
  <view class="supervise">
    <view class="table-box">
      <view class="roll">
        <view class="table">
          <view class="head">
            <view class="number">
              <text>#</text>
            </view>
            <view class="year">
              <text>取水证号</text>
            </view>
            <view class="application">
              <text>监管内容</text>
            </view>
            <view class="evaluation-form">
              <text>操作</text>
            </view>
            <view class="decision">
              <text>填报单位</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>01</text>
            </view>
            <view class="year">
              <text>9194583920028589D</text>
            </view>
            <view class="application">
              <text>日常监管</text>
            </view>
            <view class="evaluation-form">
              <text>查看</text>
            </view>
            <view class="decision">
              <text>东港镇水利管理站</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>01</text>
            </view>
            <view class="year">
              <text>9194583920028589D</text>
            </view>
            <view class="application">
              <text>日常监管</text>
            </view>
            <view class="evaluation-form">
              <text>查看</text>
            </view>
            <view class="decision">
              <text>东港镇水利管理站</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>01</text>
            </view>
            <view class="year">
              <text>9194583920028589D</text>
            </view>
            <view class="application">
              <text>日常监管</text>
            </view>
            <view class="evaluation-form">
              <text>查看</text>
            </view>
            <view class="decision">
              <text>东港镇水利管理站</text>
            </view>
          </view>
          <view class="table-r">
            <view class="number">
              <text>01</text>
            </view>
            <view class="year">
              <text>9194583920028589D</text>
            </view>
            <view class="application">
              <text>日常监管</text>
            </view>
            <view class="evaluation-form">
              <text>查看</text>
            </view>
            <view class="decision">
              <text>东港镇水利管理站</text>
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
.supervise{
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
            flex: 8;
          }
          .application{
            flex: 4;
          }
          .evaluation-form{
            flex: 2;
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
            flex: 8;
          }
          .application{
            flex: 4;
          }
          .evaluation-form{
            flex: 2;
            color: #0f6eff;
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
