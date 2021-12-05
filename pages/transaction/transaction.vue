<template>
  <view class="transaction">
    <view class="item">
      <view class="left">
        <text>取水权申请表</text>
      </view>
      <view class="right">
        <text>归档日期：2021-11-15</text>
        <u-icon name="arrow-right" color="#9ba0ab" size="12"/>
      </view>
    </view>
    <view class="item">
      <view class="left">
        <text>取水权交易证</text>
      </view>
      <view class="right">
        <text>归档日期：2021-11-15</text>
        <u-icon name="arrow-right" color="#9ba0ab" size="12"/>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data () {
    return {}
  },
  methods: {}
}
</script>

<style lang="scss">
page {
  background: #f7f7f7;
}

.transaction {
  .item {
    background-color: #ffffff;
    border-top: 2rpx solid #e6e6e6;
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
      color: #9ba0ab;

      text {
        padding-right: 18rpx;
      }
    }
  }
}
</style>
