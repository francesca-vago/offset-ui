<script setup lang="ts">
import Alert from '@/components/Alert.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
</script>

<template>
  <h1>Alert</h1>
  <SectionLayout title="Alert" class="flex flex-col gap-4">
    <Alert variant="info" message="Here is additional information that may be useful" />
    <Alert variant="error" message="An error occurred, please review the entered data." />
    <Alert variant="success" message="Operation completed successfully." />
    <Alert variant="warning" message="Please double-check the entered information." />
  </SectionLayout>
</template>
