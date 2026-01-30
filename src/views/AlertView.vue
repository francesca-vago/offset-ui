<script setup lang="ts">
import Alert from '@/components/Alert.vue'
</script>

<template>
  <h1>Alert</h1>
  <div class="flex flex-col gap-4 w-lg">
    <Alert variant="info" message="Here is additional information that may be useful" />
    <Alert variant="error" message="An error occurred, please review the entered data." />
    <Alert variant="success" message="Operation completed successfully." />
    <Alert variant="warning" message="Please double-check the entered information." />
  </div>
</template>
