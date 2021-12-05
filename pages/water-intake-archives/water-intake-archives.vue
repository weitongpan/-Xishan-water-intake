<template>
	<view class="water-intake-archives">
    <view class="search-item"
    >
      <u-row>
        <u-col span="2">
          <view class="img-box">
            <image src="../../static/public/zw.png"/>
          </view>
        </u-col>
        <u-col span="8">
          <view class="title">南国红豆控股有限公司</view>
          <view class="subtitle">取水证号：D32020578372821-D003</view>
        </u-col>
        <u-col span="2">
          <view class="source">
            <text>地表水</text>
          </view>
        </u-col>
      </u-row>
    </view>
    <view class="tag-box">
      <text>工业用水户</text>
      <text>区节水型企业</text>
      <text>高耗水行业企业</text>
    </view>
    <view class="company-info-box">
      <u-row customStyle="margin-bottom: 10px">
        <u-col span="4">
          <view class="demo-layout bg-purple-light">
            <view class="top">法定代表人</view>
            <view class="bottom">周鸣江</view>
            <image class="line" src="../../static/water-intake-archives/line2@2x.png"/>
          </view>
        </u-col>
        <u-col span="4">
          <view class="demo-layout bg-purple">
            <view class="top">水务经理</view>
            <view  class="bottom">陈玲燕</view>
            <image class="line" src="../../static/water-intake-archives/line2@2x.png"/>
          </view>
        </u-col>
        <u-col span="4">
          <view class="demo-layout bg-purple">
            <view class="top">取水证有效期至</view>
            <view class="date">2016-09-30</view>
          </view>
        </u-col>
      </u-row>
    </view>
    <view class="contact-information">
      <view class="left">
        <i class="iconfont icon-24gl-phoneLoudspeaker iphone"/>
        <text class="txt">
          联系电话：
        </text>
        <text class="number">
          18728749822
        </text>
      </view>
      <view class="right" @click="goMore">
        <text class="more">更多</text>
        <u-icon name="arrow-right" size="12" color="#9ba0ab"/>
      </view>
    </view>
    <view class="gong-ge">
      <u-grid
          :border="false"
          col="4"
      >
        <u-grid-item
            v-for="(listItem,listIndex) in gongGeData"
            :key="listIndex"
            @click="goPage(listItem.pagePath)"
        >
          <view class="gong-item">
            <image :src="listItem.path"></image>
            <text class="grid-text">{{listItem.text}}</text>
          </view>
        </u-grid-item>
      </u-grid>
    </view>
    <view class="tab-bar">
      <image src="../../static/water-intake-archives/index@2x.png" @click="goIndexPage"/>
    </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
        gongGeData: [
          {
            path: '../../static/water-intake-archives/qyxx@2x.png',
            text: '企业信息',
            pagePath: '/pages/enterprise-information/enterprise-information'
          },
          {
            path: '../../static/water-intake-archives/szlz@2x.png',
            text: '水资源论证',
            pagePath: '/pages/demonstration/demonstration'
          },
          {
            path: '../../static/water-intake-archives/qsxk@2x.png',
            text: '取水许可',
            pagePath: '/pages/water-intake-permit/water-intake-permit'
          },
          {
            path: '../../static/water-intake-archives/qsss@2x.png',
            text: '取水设施 计量监控',
            pagePath: '/pages/monitor/monitor'
          },
          {
            path: '../../static/water-intake-archives/jd@2x.png',
            text: '取水计划',
            pagePath: '/pages/water-intake-plan/water-intake-plan'
          },
          {
            path: '../../static/water-intake-archives/szyfzj@2x.png',
            text: '水资源费征缴',
            pagePath: '/pages/levy/levy'
          },
          {
            path: '../../static/water-intake-archives/jd@2x.png',
            text: '监督管理',
            pagePath: '/pages/supervise/supervise'
          },
          {
            path: '../../static/water-intake-archives/yssj@2x.png',
            text: '用水审计',
            pagePath: '/pages/audit/audit'
          },
          {
            path: '../../static/water-intake-archives/sphcs@2x.png',
            text: '水平衡测试',
            pagePath: '/pages/water-balance/water-balance'
          },
          {
            path: '../../static/water-intake-archives/jxx@2x.png',
            text: '节水型载体创建',
            pagePath: '/pages/water-conservation/water-conservation'
          },
          {
            path: '../../static/water-intake-archives/sqjy@2x.png',
            text: '水权交易',
            pagePath: '/pages/transaction/transaction'
          }
        ]
			}
		},
		methods: {
      goMore() {
        uni.navigateTo({
          url: '/pages/enterprise-information/enterprise-information'
        })
      },
      goPage(path) {
        uni.navigateTo({
          url: path
        })
      },
      goIndexPage() {
        uni.navigateTo({
          url: '/pages/index/index'
        })
      }
		}
	}
</script>

<style scoped lang="scss">
.water-intake-archives{
  .search-item{
    padding: 28rpx 26rpx 28rpx 36rpx;
    .img-box{
      image{
        width: 88rpx;
        height: 88rpx;
      }
    }
    .title{
      font-size: 34rpx;
      font-family: PingFangSC, PingFangSC-Semibold;
      font-weight: 600;
      color: #36373f;
    }
    .subtitle{
      margin-top: 4rpx;
      font-size: 24rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
      color: #9ba0ab;
    }
    .source{
      text{
        font-size: 24rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #9ba0ab;
        position: relative;
        top: 20rpx;
      }
    }
  }
  .tag-box{
    text-align: center;
    text{
      display: inline-block;
      margin: 0 12rpx;
      font-size: 20rpx;
      font-family: PingFangSC, PingFangSC-Regular;
      font-weight: 400;
    }
    text:nth-child(1){
      background: #eff7ef;
      color: #2db173;
      border-radius: 4rpx;
      padding: 4rpx 8rpx;
    }
    text:nth-child(2){
      background: #e8f0fb;
      color: #0065ff;
      border-radius: 4rpx;
      padding: 4rpx 8rpx;
    }
    text:nth-child(3){
      background: #efeff9;
      color: #4852f4;
      border-radius: 4rpx;
      padding: 4rpx 8rpx;
    }
  }
  .company-info-box{
    margin-top: 38rpx;
    .demo-layout{
      position: relative;
      view{
        text-align: center;
      }
      .top{
        font-size: 22rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #9ba0ab;
        margin-bottom: 6rpx;
      }
      .bottom{
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #0065ff;
      }
      .line{
        width: 2rpx;
        height: 40rpx;
        position: absolute;
        right: 0;
        top: 20rpx;
      }
      .date{
        color: #36373f;
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
      }
    }
  }
  .contact-information{
    display: flex;
    justify-content: space-between;
    padding: 28rpx;
    border-top: 2rpx solid #e6e6e6;
    border-bottom: 20rpx solid #f7f7f7;
    font-size: 26rpx;
    font-family: PingFangSC, PingFangSC-Regular;
    font-weight: 400;
    color: #36373f;
    .left{
      display: flex;
      .iphone{
        color: #9ba0ab;
      }
      .txt{
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #36373f;
        padding-left: 14rpx;
      }
      .number{
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #0065ff;
        padding-left: 10rpx;
      }

    }
    .right{
      display: flex;
      color: #9ba0ab;
      .more{
        padding-right: 10rpx;
      }
    }
  }
  .gong-ge{
    margin-top: 66rpx;
    .gong-item{
      text-align: center;
      height: 304rpx;
      image{
        width: 80rpx;
        height: 80rpx;
      }
      .grid-text{
        font-size: 26rpx;
        font-family: PingFangSC, PingFangSC-Regular;
        font-weight: 400;
        color: #36373f;
        display: inline-block;
        width: 130rpx;
        margin-top: 16rpx;
        text-align: center;
      }
    }
  }
  .tab-bar{
    position: fixed;
    bottom: 0;
    width: 100%;
    height: 130rpx;
    background: url("../../static/water-intake-archives/tabbar@3x.png");
    background-size: cover;
    background-position: center;
    text-align: center;
    image{
      width: 130rpx;
      height: 130rpx;
    }
  }
}
</style>
