<template>
  <h1 :class="headingClass">
    <slot name="heading"></slot>
  </h1>
</template>

<script setup>
import { computed } from 'vue'
import { twMerge } from 'tailwind-merge'

defineProps({
  headingclass: {
    type: String,
    default: ''
  }
});

const headingClass = computed(() => twMerge('text-xl md:text-2xl font-bold', headingclass))
</script>
