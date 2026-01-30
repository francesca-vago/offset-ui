<script setup lang="ts">
import Button from '../components/Button.vue'
</script>

<style scoped>
section {
  margin-bottom: 2rem;
  margin-top: 2rem;
  border: 1px solid black;
  padding: 1rem;
  background-color: var(--color-neutral-100);
  border-radius: var(--radius-sm);
}
</style>

<template>
  <h1>Buttons</h1>

  <section>
    <h2>Button Variants</h2>
    <div class="flex gap-2">
      <Button label="Click me" variant="full" />
      <Button label="Click me" variant="outline" />
      <Button label="Click me" variant="text" />
    </div>
  </section>

  <section>
    <h2>Button Sizes</h2>
    <div class="flex gap-2">
      <Button label="Click me" size="sm" />
      <Button label="Click me" size="md" />
      <Button label="Click me" size="lg" />
    </div>
  </section>

  <section>
    <h2>Button with Icon</h2>
    <div>
      <Button label="Click me" icon="pi pi-check" />
    </div>
  </section>

  <section>
    <h2>Button Disabled</h2>
    <div class="flex gap-2">
      <Button label="Click me" disabled />
    </div>
  </section>

  <section>
    <h2>Icon only</h2>
    <div>
      <Button icon="pi pi-check" />
    </div>
  </section>
</template>
