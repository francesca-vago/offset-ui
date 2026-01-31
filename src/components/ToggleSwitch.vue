<script setup lang="ts">
import ToggleSwitch from 'primevue/toggleswitch'
import { ref } from 'vue'
const checked = ref(false)
</script>

<style scoped>
.input {
  cursor: pointer;
  appearance: none;
  position: absolute;
  top: 0;
  inset-inline-start: 0;
  width: 100%;
  height: 100%;
  padding: 0;
  margin: 0;
  opacity: 0;
  z-index: 1;
  outline: 0 none;
  border-radius: var(--p-toggleswitch-border-radius);

  .slider {
    cursor: pointer;
    width: 100%;
    height: 100%;
    border-width: var(--p-toggleswitch-border-width);
    border-style: solid;
    border-color: var(--p-toggleswitch-border-color);
    background: var(--p-toggleswitch-background);
    transition:
      background var(--p-toggleswitch-transition-duration),
      color var(--p-toggleswitch-transition-duration),
      border-color var(--p-toggleswitch-transition-duration),
      outline-color var(--p-toggleswitch-transition-duration),
      box-shadow var(--p-toggleswitch-transition-duration);
    border-radius: var(--p-toggleswitch-border-radius);
    outline-color: transparent;
    box-shadow: var(--p-toggleswitch-shadow);
  }
}
</style>

<template>
  <ToggleSwitch
    v-model="checked"
    :pt="{
      // root: {
      //   class: 'slider',
      // },
      input: {
        class: 'input',
      },
      slider: {
        class: 'slider',
      },
      handle: {
        class: 'handle',
      },
    }"
    :class="['input', 'p-toggleswitch-slider', 'handle']"
  />
</template>
