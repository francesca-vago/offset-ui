<script setup lang="ts">
import Button from 'primevue/button'
defineProps<{
  label: string
  icon?: string
}>()
defineEmits<{
  click: [event: MouseEvent]
}>()
</script>

<template>
  <Button
    :label="label"
    @click="$emit('click', $event)"
    :icon="icon"
    pt:root="h-12 border-black border-2 p-2.5 bg-[#A6FAFF] hover:bg-[#79F7FF] hover:shadow-[2px_2px_0px_rgba(0,0,0,1)] active:bg-[#00E1EF] cursor-pointer"
    pt:label="font-bold text-sm"
    pt:icon="text-white text-xl"
  />
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
