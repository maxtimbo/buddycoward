<template>
  <component :is="introduction" />
  <component :is="medicaid" />
  <component :is="signage" />
</template>

<script setup lang="ts">
import { defineAsyncComponent } from 'vue'
const introduction = defineAsyncComponent(() => import('@/assets/introduction.md'))
const medicaid = defineAsyncComponent(() => import('@/assets/medicaid.md'))
const signage = defineAsyncComponent(() => import('@/assets/signage.md'))
</script>
