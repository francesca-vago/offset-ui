<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<style scoped>
section {
  margin-bottom: 2rem;
  margin-top: 2rem;
  border: 2px solid black;
  padding: 2rem;
  background-color: var(--color-neutral-100);
  border-radius: var(--radius-sm);
}
</style>

<template>
  <section class="section">
    <h2 class="mb-4">{{ title }}</h2>
    <slot />
  </section>
</template>
