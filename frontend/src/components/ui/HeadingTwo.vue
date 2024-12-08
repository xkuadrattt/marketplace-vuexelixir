<template>
  <h2 :class="headingTwoClass">
    <slot name="headingTwo"></slot>
  </h2>
</template>

<script setup>
import { computed } from 'vue'
import { twMerge } from 'tailwind-merge'

defineProps({
  headingtwoClass: {
    type: String,
    default: ''
  }
});

const headingTwoClass = computed(() => twMerge('md:text-xl font-bold', headingtwoclass))
</script>
