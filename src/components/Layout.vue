<template>
  <view class="layout_wrapper" :class="classStyle">
    <slot />
  </view>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component({})
export default class Layout extends Vue {
  @Prop(String) readonly classStyle !: String;
}
</script>

<style lang="scss" scoped>
@import "~@/assets/styles/fn.scss";

.layout_wrapper {
  height: 100vh;
  overflow: auto;
}
</style>
