<script setup lang="ts">
withDefaults(defineProps<{
  label: string
  color?: string
  href?: string
}>(), {
  color: '#b42332'
})
</script>

<template>
  <NuxtLink
    v-if="href"
    class="app-button"
    :to="href"
    :style="{ '--button-color': color }"
  >
    {{ label }}
  </NuxtLink>
  <button
    v-else
    class="app-button"
    :style="{ '--button-color': color }"
    type="button"
  >
    {{ label }}
  </button>
</template>
