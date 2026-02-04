<script setup lang="ts">
import ToggleSwitch from 'primevue/toggleswitch'
import { ref } from 'vue'
const checked = ref(false)
</script>

<style scoped>
:deep(.input) {
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
}
:deep(.slider) {
  cursor: pointer;
  width: 44px;
  height: 24px;
  border: 2px solid var(--color-text);
  background: var(--color-background);
  /* transition:
    background var(--p-toggleswitch-transition-duration),
    color var(--p-toggleswitch-transition-duration),
    border-color var(--p-toggleswitch-transition-duration),
    outline-color var(--p-toggleswitch-transition-duration),
    box-shadow var(--p-toggleswitch-transition-duration); */
  border-radius: calc(infinity * 1px);
  outline-color: transparent;
  box-shadow: var(--p-toggleswitch-shadow);
}
:deep(.handle) {
  cursor: pointer;
  width: 20px;
  height: 20px;
  border: 2px solid var(--color-text);
  background: var(--color-background);
  top: 2.5px;
  left: 4px;
  /* transition:
    background var(--p-toggleswitch-transition-duration),
    color var(--p-toggleswitch-transition-duration),
    border-color var(--p-toggleswitch-transition-duration),
    outline-color var(--p-toggleswitch-transition-duration),
    box-shadow var(--p-toggleswitch-transition-duration); */
  border-radius: 50%;
  outline-color: transparent;
  box-shadow: var(--p-toggleswitch-shadow);
  position: absolute;
}
</style>

<template>
  <ToggleSwitch
    v-model="checked"
    :pt="{
      root: {
        class: 'slider',
      },
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
  />
</template>
