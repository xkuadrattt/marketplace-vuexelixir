<template>
  <button :class="buttonClass">
    <slot name="buttonPrimary"></slot>
  </button>
</template>

<script setup>
import { computed } from 'vue'
import { twMerge } from 'tailwind-merge'

defineProps({
  buttonclass: {
    type: String,
    default: ''
  }
})

const buttonClass = computed(() => twMerge('px-2 py-1 rounded-md bg-cyan-400 hover:bg-cyan-600', buttonclass))
</script>
