<script setup lang="ts">
import Card from 'primevue/card'

defineProps<{
  header: string
  subtitle?: string
}>()
</script>

<template>
  <Card unstyled class="bg-white shadow-[4px_4px_0_0_#000000] border-black rounded-lg border">
    <template #header>
      <div class="w-full h-full">
        <img class="object-cover" src="../images/lemon-illustration.jpg" alt="Image Description" />
      </div>
    </template>
    <template #title>
      <h3 class="p-5 text-3xl mb-2 font-bold">{{ header }}</h3>
    </template>
    <template #subtitle>
      <span v-if="subtitle" class="p-5 text-sm text-neutral-500 font-medium">{{ subtitle }}</span>
    </template>
    <template #content>
      <p class="p-5 mt-1">
        Neobrutalism is an aesthetic characterized by high contrast elements, bright colors, and
        bold shapes. It is often used to make a statement, as it is meant to be eye-catching and
        stand out to the viewer. It is also used in user interface and web design, with features
        such as vibrant colors and bold shapes. Neobrutalism can also be used in print design, with
        an example being a bold shape with a vibrant color fill applied to it.
      </p>
    </template>
    <template #footer>
      <!-- <div class="">
        <Button label="Cancel" />
        <Button label="Save" />
      </div> -->
    </template>
  </Card>
</template>
