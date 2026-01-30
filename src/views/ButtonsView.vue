<script setup lang="ts">
import Button from '../components/Button.vue'
</script>

<template>
  <h1>Buttons</h1>

  <h2>Button Variants</h2>
  <div class="flex gap-2">
    <Button label="Click me" variant="full" />
    <Button label="Click me" variant="outline" />
    <Button label="Click me" variant="text" />
  </div>

  <h2>Button Sizes</h2>
  <div class="flex gap-2">
    <Button label="Click me" size="sm" />
    <Button label="Click me" size="md" />
    <Button label="Click me" size="lg" />
  </div>

  <h2>Button with Icon</h2>
  <div>
    <Button label="Click me" icon="pi pi-check" />
  </div>

  <h2>Button Disabled</h2>
  <div class="flex gap-2">
    <Button label="Click me" disabled />
  </div>

  <h2>Icon only</h2>
  <div>
    <Button icon="pi pi-check" />
  </div>
</template>
