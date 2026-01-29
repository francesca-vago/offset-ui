<script setup lang="ts">
import InputText from 'primevue/inputtext'
defineProps<{ placeholder?: string | '' }>()
</script>

<template>
  <InputText
    type="text"
    :placeholder="placeholder"
    pt:root="w-96 border-black border-2 p-2.5 focus:outline-none focus:shadow-[2px_2px_0px_rgba(0,0,0,1)] focus:bg-[#FFA6F6] active:shadow-[2px_2px_0px_rgba(0,0,0,1)]"
    pt:label="font-bold text-sm"
    pt:icon="text-white text-xl"
  />
</template>
