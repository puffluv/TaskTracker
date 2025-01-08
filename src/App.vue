<script setup>
import { CheckCircleIcon, ClockIcon, ListBulletIcon, ChartBarIcon } from '@heroicons/vue/24/outline'
import TheHeader from './components/TheHeader.vue'
import TheNav from './components/TheNav.vue'
const navItems = {
  timeline: ClockIcon,
  activities: ListBulletIcon,
  progress: ChartBarIcon,
}
</script>

<template>
  <TheHeader />

  <main class="flex flex-grow flex-col"></main>

  <TheNav />
</template>
