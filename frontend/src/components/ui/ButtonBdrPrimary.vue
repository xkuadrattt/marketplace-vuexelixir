<template>
  <button :class="buttonclass">
    <slot name="button"></slot>
  </button>
</template>

<script setup>
import { computed } from 'vue'
import { twMerge } from 'tailwind-merge'

defineProps({
  buttonClass: {
    type: String,
    default: ''
  }
})

const buttonclass = computed(() => twMerge('px-2 py-1 rounded-md border border-cyan-700', buttonClass))
</script>
