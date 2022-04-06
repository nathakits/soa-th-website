<template>
  <button class="rounded-lg p-4 text-white hover:bg-blue-600" :class="bgColor">
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    bgColor: {
      type: String,
      default: 'bg-blue-700',
    },
  },
}
</script>

<style></style>
