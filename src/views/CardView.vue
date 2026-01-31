<script setup lang="ts">
import Card from '@/components/Card.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
</script>

<template>
  <h1>Cards</h1>
  <SectionLayout title="Card with Image">
    <div class="flex gap-4 h-fit">
      <Card header="Neo Brutalism" subtitle="Card Subtitle" />
      <Card header="Neo Brutalism" subtitle="Card Subtitle" />
      <Card header="Neo Brutalism" subtitle="Card Subtitle" />
    </div>
  </SectionLayout>
</template>
