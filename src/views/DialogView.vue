<script setup lang="ts">
import Dialog from '@/components/Dialog.vue'
</script>

<style scoped>
section {
  margin-bottom: 2rem;
  margin-top: 2rem;
  border: 1px solid black;
  padding: 1rem;
  background-color: var(--color-neutral-100);
  border-radius: var(--radius-sm);
  height: 100vh;
}
</style>

<template>
  <section>
    <h2>Dialog</h2>
    <div class="w-full m-auto">
      <Dialog header="Edit Profile" />
    </div>
  </section>
</template>
