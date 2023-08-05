<script setup lang="ts">
import { computed } from 'vue'

const props = defineProps({
  class: {
    type: String,
  },
  layoutClass: {
    type: String,
  },
  leftSpan: {
    type: Number,
    default: 1,
  },
  rightSpan: {
    type: Number,
    default: 1,
  },
})

const style = computed(() => {
  return {
    gridTemplateColumns: `${props.leftSpan}fr ${props.rightSpan}fr`,
  }
})
</script>

<template>
  <div class="w-full h-full grid" :style="style" :class="props.layoutClass">
    <div class="col-left" :class="props.class">
      <slot />
    </div>
    <div class="col-right" :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>