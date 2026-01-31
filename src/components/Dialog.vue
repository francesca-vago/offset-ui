<script setup lang="ts">
import Dialog from 'primevue/dialog'
import Button from './Button.vue'

defineProps<{
  header: string
  content: string
}>()

const visible = defineModel<boolean>('visible', {
  default: false,
})
</script>

<style scoped>
:global(.p-dialog-header-icons > button) {
  cursor: pointer;
}
</style>

<template>
  <Dialog
    v-model:visible="visible"
    modal
    :pt="{
      root: 'w-96 flex px-8 py-4 bg-white border border-black shadow-[4px_4px_0_0_#000000] rounded-lg',
      header: 'w-full flex justify-between',
      title: 'text-3xl mb-2 font-bold',
      headerActions: 'p-dialog-header-icons',
      mask: 'bg-black/50',
    }"
  >
    <template #header>
      <h3 class="font-bold text-lg">{{ header }}</h3>
    </template>
    <div>
      <p class="my-4">
        {{ content }}
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
