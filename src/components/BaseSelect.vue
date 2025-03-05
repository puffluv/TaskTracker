<script setup>
import { TrashIcon } from '@heroicons/vue/24/outline'
import BaseButton from './BaseButton.vue'
defineProps(['placeholder', 'options', 'selected'])
</script>
<template>
  <div class="flex gap-2">
    <BaseButton>
      <TrashIcon class="h-6" />
    </BaseButton>
    <select class="w-full truncate rounded bg-gray-100 py-1 px-2 text-xl">
      <option disable selected value="">{{ placeholder }}</option>
      <option
        v-for="{ value, label } in options"
        :key="value"
        :value="value"
        :selected="value === selected"
      >
        {{ label }}
      </option>
    </select>
  </div>
</template>
