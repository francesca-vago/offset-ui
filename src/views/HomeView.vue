<script setup lang="ts">
import SectionLayout from '../layouts/SectionLayout.vue'
</script>

<template>
  <h1>Overview</h1>

  <SectionLayout title="Typography">
    <h1>This is Heading 1</h1>
    <h2>This is Heading 2</h2>
    <h3>This is Heading 3</h3>
    <h4>This is Heading 4</h4>
    <h5>This is Heading 5</h5>
    <h6>This is Heading 6</h6>
    <p>This is a paragraph</p>
    <span>This is a span</span>
  </SectionLayout>

  <SectionLayout title="Colors">
    <div class="flex gap-3 mb-3">
      <div class="bg-red-200 w-10 h-10"></div>
      <div class="bg-green-200 w-10 h-10"></div>
      <div class="bg-blue-200 w-10 h-10"></div>
      <div class="bg-yellow-200 w-10 h-10"></div>
      <div class="bg-purple-200 w-10 h-10"></div>
      <div class="bg-pink-200 w-10 h-10"></div>
    </div>
    <div class="flex gap-3 mb-3">
      <div class="bg-neutral-950 w-10 h-10"></div>
      <div class="bg-stone-200 w-10 h-10"></div>
      <div class="bg-gray-500 w-10 h-10"></div>
    </div>
  </SectionLayout>

  <SectionLayout title="Spacing">
    <div class="w-10 h-10"></div>
  </SectionLayout>
</template>
