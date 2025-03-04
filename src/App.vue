<script setup>
import { CheckCircleIcon, ClockIcon, ListBulletIcon, ChartBarIcon } from '@heroicons/vue/24/outline'
import TheHeader from './components/TheHeader.vue'
import TheNav from './components/TheNav.vue'
import TheTimeline from './pages/TheTimeline.vue'
import TheActivities from './pages/TheActivities.vue'
import TheProgress from './pages/TheProgress.vue'
import { ref } from 'vue'
import { PAGE_ACTIVITIES, PAGE_TIMELINE, PAGE_PROGRESS } from './constants'
import { normalizePageHash, generateTimelineItems } from './functions'

const currentPage = ref(normalizePageHash())

const timelineItems = generateTimelineItems()

function goTo(page) {
  currentPage.value = page
}
</script>

<template>
  <TheHeader @go-to-timeline="goTo(PAGE_TIMELINE)" @go-to-progress="goTo(PAGE_PROGRESS)" />

  <main class="flex flex-grow flex-col">
    <TheTimeline v-show="currentPage == PAGE_TIMELINE" v-bind:timeline-items="timelineItems" />
    <TheActivities v-show="currentPage == PAGE_ACTIVITIES" />
    <TheProgress v-show="currentPage == PAGE_PROGRESS" />
  </main>

  <TheNav :current-page="currentPage" @navigate="goTo($event)" />
</template>
