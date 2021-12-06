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
          <view class="table-r" v-for="(item, index) in tableData" :key="index">
            <view class="number">
              <text>{{ item.id }}</text>
            </view>
            <view class="year">
              <text>{{ item.t1 }}</text>
            </view>
            <view class="application">
              <text>{{ item.t2 }}</text>
            </view>
            <view class="evaluation-form">
              <text @click="goPage">{{ item.t3 }}</text>
            </view>
            <view class="decision">
              <text>{{ item.t4 }}</text>
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
      tableData: [
        {
          id: '01',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '02',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '03',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '04',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '05',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '06',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '07',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        },
        {
          id: '08',
          t1: '9194583920028589D',
          t2: '日常监管',
          t3: '查看',
          t4: '东港镇水利管理站'
        }
      ]
    }
  },
  methods: {
    goPage() {
      uni.navigateTo({
        url: '/pages/supervision-details/supervision-details'
      })
    },
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
