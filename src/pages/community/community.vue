<template>
  <view class="community_main_wrapper">
    <view class="main">
      <view
        class="card"
        v-for="(item, index) in cardList"
        :key="index"
      >
        <image class="avatar" src="" />
        <text class="name">努力了吗梁同学</text>
        <view class="content"></view>
      </view>
    </view>
  </view>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class community extends Vue {
  cardList = [1, 2, 3, 4];
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

.community_main_wrapper {
  overflow: auto;
  height: 100vh;
  padding: rpx(12);
  > .main {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    > .card {
      $card: rpx(170);
      display: flex;
      flex-direction: column;
      align-items: center;
      overflow: hidden;
      width: $card;
      min-height: $card;
      margin-bottom: rpx(10);
      border-radius: rpx(10);
      border: rpx(1) solid #000;
      > .avatar {
        $avatar: rpx(50);
        width: $avatar;
        height: $avatar;
        margin-top: rpx(10);
        border-radius: 50%;
        background: skyblue;
      }
      > .name {
        margin: rpx(10) 0;
      }
      > .content {
        flex-grow: 1;
        width: 100%;
        border-top: rpx(1) solid #000;
      }
    }
  }
}
</style>
