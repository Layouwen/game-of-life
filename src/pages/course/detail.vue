<template>
  <Layout class-style="layout" class="course_detail_wrapper">
    我是详情页
  </Layout>
</template>

<script lang="ts">
import Layout from '@/components/Layout.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {Layout},
})
export default class detail extends Vue {
}
</script>

<style lang="scss" scoped>
::v-deep .layout {
  background: skyblue;
}

.course_detail_wrapper {
}
</style>
