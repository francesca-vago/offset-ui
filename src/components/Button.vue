<script setup lang="ts">
import Button from 'primevue/button'
type Variant = 'full' | 'outline' | 'text'
type Size = 'sm' | 'md' | 'lg'

withDefaults(
  defineProps<{
    variant?: Variant
    size?: Size
    label?: string
    icon?: string
    disabled?: boolean
  }>(),
  {
    variant: 'full',
    size: 'md',
    disabled: false,
  },
)

defineEmits<{
  click: [event: MouseEvent]
}>()
</script>

<style scoped>
.full {
  background-color: var(--primary);
}

.outline {
  background-color: white;
}

.text {
  background-color: transparent;
  border: none;
  box-shadow: none;

  &:hover {
    text-decoration: underline;
    text-underline-offset: 4px;
    text-decoration-style: wavy;
    text-decoration-thickness: 2px;
  }
}

.sm {
  padding: 0.25rem 0.75rem;
  font-size: 0.75rem;
  line-height: 1rem;
}

.md {
  padding: 0.5rem 1.5rem;
  font-size: 1rem;
}

.lg {
  padding: 0.5rem 2.5rem;
  font-size: 1.25rem;
}

.disabled {
  cursor: not-allowed;
  background-color: var(--color-neutral-200);
  color: black;
  opacity: 0.8;
}

.icon-only {
  padding: 0.25rem 0.5rem;
}
</style>

<template>
  <Button
    :label="label"
    @click="$emit('click', $event)"
    :icon="icon"
    :disabled="disabled"
    pt:root="h-fit space-x-2 border-black border-2 hover:bg-[#79F7FF] shadow-[4px_4px_0px_rgba(0,0,0,1)] active:bg-[#00E1EF] active:shadow-none cursor-pointer rounded-sm select-none"
    pt:label="font-bold"
    pt:icon="!font-bold"
    :class="[variant, size, disabled ? 'disabled' : '', icon && !label ? 'icon-only' : '']"
  />
</template>
