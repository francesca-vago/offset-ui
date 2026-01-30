<script setup lang="ts">
import Card from '@/components/Card.vue'
</script>

<template>
  <section class="bg-neutral-100 border border-black p-4 rounded-sm">
    <h1>Card</h1>
    <div class="flex gap-4 bg-neutral-100 border border-black p-4 rounded-sm h-fit">
      <Card header="Neo Brutalism" subtitle="Card Subtitle" />
      <Card header="Neo Brutalism" subtitle="Card Subtitle" />
      <Card header="Neo Brutalism" subtitle="Card Subtitle" />
    </div>
  </section>
</template>
