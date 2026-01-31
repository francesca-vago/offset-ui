<script setup lang="ts">
import Input from '@/components/Input.vue'
import TextArea from '@/components/TextArea.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
</script>

<template>
  <MainLayout title="Inputs">
    <SectionLayout title="Input Text">
      <Input placeholder="Enter your name" />
    </SectionLayout>
    <SectionLayout title="Textarea">
      <TextArea placeholder="Enter your message" />
    </SectionLayout>
  </MainLayout>
</template>
