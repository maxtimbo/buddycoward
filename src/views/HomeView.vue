<template>
  <div class="paralax">
    <IntoSplash ref="bannerComponent" />
  </div>
  <div class="body-content" :style="{ marginTop: bannerHeight + 'px' }">
    <TextBlock />
    <MediaLinks />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted, nextTick, watch } from 'vue';
import IntoSplash from '../components/IntoSplash.vue';
import TextBlock from '../components/TextBlock.vue';
import MediaLinks from '../components/MediaLinks.vue';

const bannerComponent = ref<{ bannerElement: HTMLElement } | null>(null);
const bannerHeight = ref(0);

const updateBannerHeight = () => {
  if (bannerComponent.value?.bannerElement) {
    bannerHeight.value = bannerComponent.value.bannerElement.offsetHeight + 10;
    console.log(bannerHeight.value);
  }
};

watch(bannerComponent, (newVal) => {
  if (newVal) {
    nextTick(updateBannerHeight);
  }
});

onMounted(() => {
  nextTick(() => {
    setTimeout(updateBannerHeight, 100);
  });
  window.addEventListener('resize', updateBannerHeight);
});

onUnmounted(() => {
  window.removeEventListener('resize', updateBannerHeight);
});
</script>
