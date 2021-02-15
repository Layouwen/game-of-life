<template>
  <view class="tab_list">
    <view
      class="tab_list_item"
      v-for="tab in tabList"
    >
      {{ tab }}
    </view>
  </view>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class TabList extends Vue {
  tabList = [1, 2];
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

.tab_list {
  display: flex;
  justify-content: space-between;
  > .tab_list_item {
    width: rpx(170);
    height: rpx(79);
    border: 1px solid #707070;
    border-radius: rpx(10);
    background: #fff;
  }
}
</style>
