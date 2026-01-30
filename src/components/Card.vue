<script setup lang="ts">
import Card from 'primevue/card'
import Button from '@/components/Button.vue'

defineProps<{
  header: string
  subtitle?: string
}>()
</script>

<template>
  <Card
    unstyled
    class="bg-white shadow-[4px_4px_0_0_#000000] border-black rounded-lg border overflow-hidden h-fit"
  >
    <template #header>
      <div>
        <img class="w-full h-auto" src="../images/lemon-illustration.jpg" alt="Image Description" />
      </div>
    </template>
    <template #title>
      <h5 class="px-5 pt-5">{{ header }}</h5>
    </template>
    <template #subtitle>
      <span v-if="subtitle" class="px-5 text-neutral-500 font-medium">{{ subtitle }}</span>
    </template>
    <template #content>
      <p class="px-5 mt-1">
        Neobrutalism is an aesthetic characterized by high contrast elements, bright colors, and
        bold shapes. It is often used to make a statement, as it is meant to be eye-catching and
        stand out to the viewer.
      </p>
    </template>
    <template #footer>
      <div class="flex justify-end gap-2 px-5 py-5">
        <Button label="Cancel" size="sm" variant="outline" />
        <Button label="Save" size="sm" variant="full" />
      </div>
    </template>
  </Card>
</template>
