<script setup>
defineProps({
  type: {
    type: String,
    default: () => '',
  },
})
</script>

<template>
  <div
    class="alert"
    :class="[type]"
  >
    <slot mdc-unwrap="p" />
  </div>
</template>

<style scoped lang="postcss">
.alert {
  @apply text-black p-2 border dark:text-white rounded;
}
.warning {
  @apply bg-orange-100 border-orange-200 dark:bg-orange-900 dark:border-orange-800;
}
</style>
