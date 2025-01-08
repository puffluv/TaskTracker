<template>
  <a href="" class="text=sm">
    <div v-if="false" class="flex items-center gap-1">
      All tasks done!
      <CheckCircleIcon class="h-7 text-green-900"></CheckCircleIcon>
    </div>
    <div v-else class="flex items-center gap-1">
      <div>Progress: <span class="font-mono">20%</span></div>
      <div class="h-3 w-3 rounded-full bg-red-900"></div>
    </div>
  </a>
</template>
