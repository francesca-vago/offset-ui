<script setup lang="ts">
import Menu from 'primevue/menu'
import type { MenuItem } from 'primevue/menuitem'

defineProps<{
  items: MenuItem[]
}>()
</script>

<template>
  <Menu
    :model="items"
    :pt="{
      content: 'border border-black w-auto',
    }"
  >
    <template #item="{ item, props }">
      <slot name="item" :item="item" :props="props" />
    </template>
  </Menu>
</template>
