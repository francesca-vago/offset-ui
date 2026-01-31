<script setup lang="ts">
import Card from '@/components/Card.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
</script>

<template>
  <MainLayout title="Cards">
    <SectionLayout title="Card with Image">
      <div class="flex gap-4 h-fit">
        <Card header="Neo Brutalism" subtitle="Card Subtitle" />
        <Card header="Neo Brutalism" subtitle="Card Subtitle" />
        <Card header="Neo Brutalism" subtitle="Card Subtitle" />
      </div>
    </SectionLayout>
  </MainLayout>
</template>
