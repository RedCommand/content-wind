<script setup lang="ts">
defineProps({
  padded: {
    type: Boolean,
    required: false,
    default: false
  }
})
</script>

<template>
  <div
    :class="[padded ? 'px-4 sm:px-6' : '']"
    class="mx-auto pb-[72px]"
  >
    <slot />
  </div>
</template>
