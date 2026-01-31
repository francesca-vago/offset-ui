<script setup lang="ts">
import Input from '@/components/Input.vue'
import TextArea from '@/components/TextArea.vue'
</script>

<template>
  <section class="bg-neutral-100 border border-black p-4 rounded-sm">
    <h1>Inputs</h1>
    <Input placeholder="Enter your name" class="mb-4" />
    <TextArea placeholder="Enter your message" class="mb-4" />
  </section>
</template>
