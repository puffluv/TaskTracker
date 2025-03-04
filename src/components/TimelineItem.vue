<script setup>
import { TrashIcon } from '@heroicons/vue/24/outline'

const props = defineProps(['timelineItem'])

const hourLinkClasses = [
  'absolute -top-4 left-1/2 -translate-x-1/2 rounded  px-2 font-mono text-lg',
  props.timelineItem.hour === new Date().getHours()
    ? 'bg-green-900 text-white font-black'
    : 'bg-green-700 text-white',
]

const options = [
  { value: 1, label: 'Code' },
  { value: 2, label: 'Learn' },
  { value: 3, label: 'Work' },
]
</script>
<template>
  <li class="relative flex flex-col gap-2 border-t border-gray-200 py-10 px-4">
    <a href="#" v-bind:class="hourLinkClasses">{{ timelineItem.hour }}:00</a>
    <div class="flex gap-2">
      <button
        class="rounded bg-gray-100 p-3 enabled:hover:bg-gray-200 disabled:cursor-not-allowed disabled:opacity-50"
      >
        <TrashIcon class="h-6" />
      </button>
      <select name="" id="" class="w-full truncate rounded bg-gray-100 py-1 px-2 text-xl">
        <option disable selected value="">Chill</option>
        <option v-for="{ value, label } in options" :key="value" :value="value">{{ label }}</option>
      </select>
    </div>
  </li>
</template>
