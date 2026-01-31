<script setup lang="ts">
import Dialog from '@/components/Dialog.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
</script>

<template>
  <MainLayout title="Dialog">
    <SectionLayout title="Dialog Button">
      <Dialog header="Edit Profile" />
    </SectionLayout>
  </MainLayout>
</template>
