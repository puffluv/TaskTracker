<script setup>
import { CheckCircleIcon } from '@heroicons/vue/24/outline'
import TheLogo from './TheLogo.vue'
import TheHeaderProgress from './TheHeaderProgress.vue'
</script>
<template>
  <header class="sticky top-0 z-20 flex items-center justify-between border-b bg-white p-3">
    <TheLogo />
    <TheHeaderProgress />
  </header>
</template>
