<script setup lang="ts">
import Button from '../components/Button.vue'
import SectionLayout from '../layouts/SectionLayout.vue'
</script>

<template>
  <h1>Buttons</h1>

  <SectionLayout title="Button Variants">
    <div class="flex gap-2">
      <Button label="Click me" variant="full" />
      <Button label="Click me" variant="outline" />
      <Button label="Click me" variant="text" />
    </div>
  </SectionLayout>

  <SectionLayout title="Button Sizes">
    <div class="flex gap-2">
      <Button label="Click me" size="sm" />
      <Button label="Click me" size="md" />
      <Button label="Click me" size="lg" />
    </div>
  </SectionLayout>

  <SectionLayout title="Button with Icon">
    <div>
      <Button label="Click me" icon="pi pi-check" />
    </div>
  </SectionLayout>

  <SectionLayout title="Button Disabled">
    <div class="flex gap-2">
      <Button label="Click me" disabled />
    </div>
  </SectionLayout>

  <SectionLayout title="Icon only">
    <div>
      <Button icon="pi pi-check" />
    </div>
  </SectionLayout>
</template>
