<template>
  <Layout class-style="layout" class="mine_main_wrapper">

  </Layout>
</template>

<script lang="ts">
import Layout from '@/components/Layout.vue';
import { Component, Vue } from 'vue-property-decorator';

@Component({
  components: {Layout},
})
export default class mine extends Vue {
}
</script>

<style lang="scss" scoped>
::v-deep .layout {
}
.mine_main_wrapper {

}
</style>
