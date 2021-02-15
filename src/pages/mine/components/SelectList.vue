<template>
  <view class="select_list">
    <view
      class="select_list_item"
      v-for="select in selectList"
      :key="select.title"
    >
      <text>{{ select.title }}</text>
      <view class="icon_right" />
    </view>
  </view>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class SelectList extends Vue {
  selectList = [
    {
      title: '基本信息',
      link: null,
    },
    {
      title: '公开的进程',
      link: null,
    },
    {
      title: '设置联合进程',
      link: null,
    },
    {
      title: '备份/同步',
      link: null,
    },
  ];
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

.select_list {
  display: flex;
  flex-direction: column;
  margin-top: rpx(20);
  > .select_list_item {
    display: flex;
    justify-content: space-between;
    padding: rpx(13);
    margin-bottom: rpx(10);
    box-shadow: 0 0 rpx(8) rgba(0, 0, 0, .16);
    border-radius: rpx(10);
    background: #fff;
    > .icon_right {
      $iconRight: rpx(20);
      width: $iconRight;
      height: $iconRight;
      background: url("~@/assets/icons/right.png") no-repeat 0 0;
      background-size: 100%;
    }
  }
}
</style>
