<template>
  <div class="banner-wrap" ref="bannerElement">
    <img alt="chicken" class="logo" src="@/assets/chicken.svg" />
    <div class="banner">
      <h2><span>Buddy</span></h2>
      <h1>Coward</h1>
      <h5><span>Face your Constituency</span></h5>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, defineExpose } from 'vue';

const bannerElement = ref<HTMLElement | null>(null);

defineExpose({ bannerElement });
</script>

<style>

</style>
