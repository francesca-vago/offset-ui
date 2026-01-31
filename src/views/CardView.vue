<script setup lang="ts">
import Card from '@/components/Card.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
</script>

<template>
  <MainLayout title="Cards">
    <SectionLayout title="Card with Image">
      <div class="w-80 mx-auto">
        <Card
          title="Neo Brutalism"
          subtitle="31/01/2026"
          image="src/images/lemon-illustration.jpg"
          content="Neobrutalism is an aesthetic characterized by high contrast elements, bright colors, and bold shapes. It is often used to make a statement, as it is meant to be eye-catching and stand out to the viewer."
        />
      </div>
    </SectionLayout>
    <SectionLayout title="Card without Image">
      <div class="w-80 mx-auto">
        <Card
          title="Neo Brutalism"
          subtitle="31/01/2026"
          content="Neobrutalism is an aesthetic characterized by high contrast elements, bright colors, and bold shapes. It is often used to make a statement, as it is meant to be eye-catching and stand out to the viewer."
        />
      </div>
    </SectionLayout>
  </MainLayout>
</template>
