<template>
  <Layout class="course_main_wrapper" class-style="layout">
    <view
      class="card"
      v-for="(item, index) in cardList"
      :key="index"
      @click="onLinkPage"
    >
      <image class="logo" src="" />
      <text class="title">成长</text>
      <text class="count">10/100</text>
      <text class="percent">10%</text>
    </view>
  </Layout>
</template>

<script lang="ts">
import Layout from '@/components/Layout.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {Layout},
})
export default class course extends Vue {
  cardList = [1, 2, 3, 4, 5, 6, 7, 8];

  onLinkPage () {
    uni.navigateTo({url: '/pages/course/detail'});
  }
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

::v-deep .layout {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: rpx(12);
}

.course_main_wrapper {
  .card {
    flex-shrink: 0;
    display: flex;
    align-items: center;
    width: rpx(349);
    height: rpx(94);
    padding: rpx(20);
    margin-bottom: rpx(10);
    font-size: rpx(20);
    border: rpx(1) solid #707070;
    border-radius: rpx(10);
    background: #fff;
    > .logo {
      $logo: rpx(54);
      width: $logo;
      height: $logo;
      margin-right: rpx(20);
      border: rpx(1) solid #707070;
      border-radius: rpx(10);
      background: #FFFFFF;
    }
    > .title {
      flex-grow: 1;
    }
    > .count {
      margin: 0 rpx(20);
    }
  }
}
</style>
