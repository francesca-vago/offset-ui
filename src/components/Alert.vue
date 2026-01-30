<script setup lang="ts">
type Variant = 'info' | 'error' | 'success' | 'warning'

withDefaults(
  defineProps<{
    variant: Variant
    message: string
  }>(),
  {
    variant: 'info',
  },
)

const type: Record<Variant, { icon: string; label: string }> = {
  info: {
    icon: 'pi-info-circle',
    label: 'Info',
  },
  error: {
    icon: 'pi-times-circle',
    label: 'Error',
  },
  success: {
    icon: 'pi-check-circle',
    label: 'Success',
  },
  warning: {
    icon: 'pi-exclamation-triangle',
    label: 'Warning',
  },
}
</script>

<style scoped>
.base {
  border: 2px solid black;
  border-radius: 4px;
  color: black;
  padding: 0.5rem 1rem;
  display: flex;
  justify-content: space-between;
  box-shadow: 4px 4px rgba(0, 0, 0);
  background-color: white;
}

.error {
  background-color: var(--danger);
}

.success {
  background-color: var(--success);
}

.warning {
  background-color: var(--warning);
}
</style>

<template>
  <div :class="['base', variant]">
    <div class="flex gap-1 items-center">
      <span :class="type[variant].icon" class="pi me-3"></span>
      <p class="text-sm">
        <strong>{{ type[variant].label }}:</strong> {{ message }}
      </p>
    </div>
    <button data-close="#alert-closer" class="cursor-pointer">
      <i class="pi pi-times text-sm"></i>
    </button>
  </div>
</template>
