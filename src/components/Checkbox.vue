<script setup lang="ts">
import Checkbox from 'primevue/checkbox'

const checked = defineModel<boolean>('checked', {
  default: false,
})

defineProps<{
  label: string
  inputId: string
  name: string
  value: string
}>()
</script>

<template>
  <div class="flex items-center gap-2">
    <Checkbox
      v-model="checked"
      :inputId="inputId"
      :name="name"
      :value="value"
      :pt="{
        root: 'appearance-none outline-none block relative text-center cursor-pointer w-5 h-5 before:rounded-sm before:block before:absolute before:bg-white before:w-5 before:h-5 before:rounded-sm before:border-black before:border-2 before:hover:shadow-[2px_2px_0px_rgba(0,0,0,1)] after:block after:absolute after:left-1.5 after:top-0.5 after:w-2 after:h-3 after:border-black after:border-r-2 after:border-b-2 after:origin-center after:rotate-45',
      }"
      :class="[
        checked ? 'after:opacity-1 before:checked:bg-[var(--bg-background)]' : 'after:opacity-0',
      ]"
    />
    <label :for="inputId"> {{ label }} </label>
  </div>
</template>
