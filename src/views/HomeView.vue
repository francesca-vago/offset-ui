<script setup lang="ts"></script>

<style scoped>
section {
  border: 1px solid black;
  padding: 1rem;
  background-color: var(--color-neutral-100);
  border-radius: var(--radius-sm);
  margin-bottom: 2rem;
}

.section-title {
  margin-bottom: 2rem;
}
</style>

<template>
  <h1>Overview</h1>

  <section>
    <h2 class="section-title">Typography</h2>
    <h1>This is Heading 1</h1>
    <h2>This is Heading 2</h2>
    <h3>This is Heading 3</h3>
    <h4>This is Heading 4</h4>
    <h5>This is Heading 5</h5>
    <h6>This is Heading 6</h6>
    <p>This is a paragraph</p>
    <span>This is a span</span>
  </section>

  <section>
    <h2 class="section-title">Colors</h2>
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
  </section>

  <section>
    <h2 class="section-title">Spacing</h2>
    <div class="w-10 h-10"></div>
  </section>
</template>
