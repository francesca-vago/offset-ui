<script setup lang="ts">
import Menubar from 'primevue/menubar'
import { ref } from 'vue'

const items = ref([
  {
    label: 'Home',
    icon: 'pi pi-home',
  },
  {
    label: 'Features',
    icon: 'pi pi-star',
  },
  {
    label: 'Projects',
    icon: 'pi pi-search',
  },
  {
    label: 'Contact',
    icon: 'pi pi-envelope',
  },
])
</script>

<style scoped>
.card {
  border: 1px solid black;
  padding: 0.75rem 1rem;
}
</style>

<template>
  <div class="card">
    <Menubar
      :model="items"
      :pt="{
        root: { class: 'flex justify-between' },
        rootList: { class: 'flex gap-1 items-center justify-end' },
        button: { class: 'hidden' },
        itemLink: { class: 'flex gap-2 items-center px-3 py-2 cursor-pointer' },
      }"
    >
      <template #start>
        <div class="w-[calc(250px_-_4rem)]">
          <img src="../images/logo-color-horizontal.png" alt="Logo" class="w-fit" />
        </div>
      </template>
    </Menubar>
  </div>
</template>
