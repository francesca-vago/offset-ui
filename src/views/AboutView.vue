<script setup lang="ts">
import { ref } from 'vue'

const name = ref('')

function handleChange(event: Event) {
  name.value = (event.target as HTMLInputElement).value
}
</script>

<template>
  <input type="text" @change="handleChange" :value="name" />
  <button @click="console.log(name)">Saluta</button>
</template>
