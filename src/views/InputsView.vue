<script setup lang="ts">
import Input from '@/components/Input.vue'
import TextArea from '@/components/TextArea.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
</script>

<template>
  <h1>Inputs</h1>
  <SectionLayout title="Input Text">
    <Input placeholder="Enter your name" />
  </SectionLayout>
  <SectionLayout title="Textarea">
    <TextArea placeholder="Enter your message" />
  </SectionLayout>
</template>
