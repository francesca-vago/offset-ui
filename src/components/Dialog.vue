<script setup lang="ts">
import Dialog from 'primevue/dialog'
import Button from './Button.vue'
import { ref } from 'vue'

defineProps<{
  header: string
}>()

const visible = ref(false)
</script>

<template>
  <Button @click="visible = true" label="Show Dialog" />
  <Dialog
    v-model:visible="visible"
    modal
    pt:root="w-96 flex px-8 py-4 bg-white border border-black shadow-[4px_4px_0_0_#000000] rounded-lg"
    :pt="{
      header: 'w-full flex justify-between',
      title: 'text-3xl mb-2 font-bold',
      headerActions: 'cursor-pointer',
    }"
  >
    <template #header>
      <h3 class="font-bold text-lg">{{ header }}</h3>
    </template>
    <div>
      <p class="my-4">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
        labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
        laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
        voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
        cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
      </p>
    </div>
    <template #footer>
      <div class="flex justify-end gap-4">
        <Button label="Cancel" @click="visible = false" variant="outline" />
        <Button label="Save" @click="visible = false" />
      </div>
    </template>
  </Dialog>
</template>
