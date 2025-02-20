<script>
export default {
  inheritAttrs: false,
}
</script>
<template>
  <li class="flex-1">
    <a v-bind="$attrs" class="flex flex-col items-center p2 text-xs capitalize">
      <slot></slot>
    </a>
  </li>
</template>
