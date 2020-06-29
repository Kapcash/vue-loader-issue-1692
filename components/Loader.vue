<template>
  <div>
    <!-- Removing the class attributte here fixes the problem -->
    <div v-if="loading" class="">
      LOADING...
    </div>
    <!-- Removing the v-if / v-else also fixes the problem -->
    <slot v-else></slot>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default class Loader extends Vue {
  loading = true;
  mounted() {
    setTimeout(() => this.loading = false, 1000);
  }
}
</script>

<style>
</style>
