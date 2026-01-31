<script setup lang="ts">
defineProps<{
  title: string
}>()
</script>

<style scoped>
main {
  padding: 4rem;
  background-color: var(--color-blue-200);
  border-left: 1px solid black;
  flex-grow: 1;
}
</style>

<template>
  <main class="main">
    <h1 class="mb-4">{{ title }}</h1>
    <slot />
  </main>
</template>
