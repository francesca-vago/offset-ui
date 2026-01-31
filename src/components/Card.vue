<script setup lang="ts">
import Card from 'primevue/card'
import Button from '@/components/Button.vue'

defineProps<{
  title: string
  subtitle?: string
  content?: string
  image?: string
  noFooter?: boolean
}>()
</script>

<template>
  <Card
    unstyled
    class="shadow-[4px_4px_0_0_#000000] border-black rounded-sm border-2 overflow-hidden w-full max-w-2xl h-fit"
  >
    <template #header>
      <div class="w-full h-full">
        <img v-if="image" class="w-full h-full object-cover" :src="image" alt="Image Description" />
      </div>
    </template>
    <template #title>
      <h4 class="px-5 pt-5">{{ title }}</h4>
    </template>
    <template #subtitle>
      <span v-if="subtitle" class="px-5 text-neutral-500 font-medium">{{ subtitle }}</span>
    </template>
    <template #content>
      <p v-if="content" class="px-5 mt-1 !text-xs text-justify text-wrap">
        {{ content }}
      </p>
    </template>
    <template #footer>
      <div v-if="!noFooter" class="flex justify-end gap-2 px-5 py-5">
        <Button label="Read More" size="sm" variant="text" />
      </div>
    </template>
  </Card>
</template>
