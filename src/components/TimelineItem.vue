<script setup>
const props = defineProps(['timelineItem'])

const hourLinkClasses = [
  'absolute -top-4 left-1/2 -translate-x-1/2 rounded  px-2 font-mono text-lg',
  props.timelineItem.hour === new Date().getHours()
    ? 'bg-green-900 text-white font-black'
    : 'bg-green-700 text-white',
]
</script>
<template>
  <li class="relative flex flex-col gap-2 border-t border-gray-200 py-10 px-4">
    <a href="#" v-bind:class="hourLinkClasses">{{ timelineItem.hour }}:00</a>
  </li>
</template>
