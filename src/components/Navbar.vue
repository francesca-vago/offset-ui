<script setup lang="ts">
import Menubar from 'primevue/menubar'
import { ref } from 'vue'

const items = ref([
  {
    label: 'Github',
    icon: 'pi pi-star',
    url: 'https://github.com/francesca-vago',
  },
  {
    label: 'Contact',
    icon: 'pi pi-envelope',
  },
])
</script>

<style scoped>
.card {
  border-bottom: 2px solid black;
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
      <template #item="{ item, props, hasSubmenu, root }">
        <a
          v-ripple
          class="flex items-center hover:underline hover:underline-offset-4 decoration-wavy decoration-2 font-bold"
          v-bind="props.action"
          :href="item.url"
        >
          <span>{{ item.label }}</span>
          <i
            v-if="hasSubmenu"
            :class="[
              'pi pi-angle-down ml-auto',
              { 'pi-angle-down': root, 'pi-angle-right': !root },
            ]"
          ></i>
        </a>
      </template>
    </Menubar>
  </div>
</template>
