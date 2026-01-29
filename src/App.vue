<script setup lang="ts">
import { RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
</script>

<template>
  <aside class="w-[250px] h-full">
    <Menu />
  </aside>
  <main class="flex-1">
    <RouterView />
  </main>
</template>
