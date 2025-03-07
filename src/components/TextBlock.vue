<template>
  <component :is="markdownComponent" />
</template>

<script setup lang="ts">
import { defineAsyncComponent } from 'vue'
const markdownComponent = defineAsyncComponent(() => import('@/assets/stain.md'))
</script>
