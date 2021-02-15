<template>
  <view class="data_show">
    <view
      class="item"
      v-for="item in dataShow"
      :key="item.title"
    >
      <text class="number">{{ item.number }}</text>
      <text class="title">{{ item.title }}</text>
    </view>
  </view>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class DataShow extends Vue {
  dataShow = [
    {
      number: 10,
      title: '已完成进程',
    },
    {
      number: 203,
      title: '好友',
    },
    {
      number: 20,
      title: '总进程',
    },
  ];
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

.data_show {
  display: flex;
  padding-bottom: rpx(18);
  margin-top: rpx(50);
  font-size: rpx(13);
  > .item {
    $itemWidth: 100% / 3;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: $itemWidth;
    > .number {
      font-size: rpx(28);
    }
  }
}
</style>
