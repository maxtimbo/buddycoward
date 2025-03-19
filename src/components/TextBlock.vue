<template>
  <component :is="introduction" />
  <component :is="impeach" />
  <component :is="medicaid" />
  <component :is="signage" />
</template>

<script setup lang="ts">
import { defineAsyncComponent } from 'vue'
const introduction = defineAsyncComponent(() => import('@/assets/introduction.md'))
const impeach = defineAsyncComponent(() => import('@/assets/impeach.md'))
const medicaid = defineAsyncComponent(() => import('@/assets/medicaid.md'))
const signage = defineAsyncComponent(() => import('@/assets/signage.md'))
</script>
