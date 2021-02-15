<template>
  <Layout class-style="layout" class="mine_main_wrapper">
    <view class="wrapper">
      <image class="avatar" src="" />
      <DataShow />
      <TabList />
      <SelectList />
    </view>
  </Layout>
</template>

<script lang="ts">
import Layout from '@/components/Layout.vue';
import DataShow from '@/pages/mine/components/DataShow.vue';
import SelectList from '@/pages/mine/components/SelectList.vue';
import TabList from '@/pages/mine/components/TabList.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {SelectList, TabList, DataShow, Layout},
})
export default class mine extends Vue {
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

::v-deep .layout {
  display: flex;
  flex-direction: column;
  background: #D86363;
}


.mine_main_wrapper {
  .wrapper {
    position: relative;
    flex-grow: 1;
    padding: 0 rpx(12);
    margin-top: rpx(59);
    border-radius: rpx(20) rpx(20) 0 0;
    background: #fff;
    > .avatar {
      $avatar: rpx(88);
      position: absolute;
      top: $avatar / -2;
      left: 50%;
      transform: translateX(-50%);
      height: $avatar;
      width: $avatar;
      border-radius: 50%;
      background: #999;
    }

  }
}
</style>
