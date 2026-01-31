<script setup lang="ts">
import Dialog from '@/components/Dialog.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
import Button from '@/components/Button.vue'
import { ref } from 'vue'

const visible = ref(false)
</script>

<template>
  <MainLayout title="Dialog">
    <SectionLayout title="Dialog Button">
      <div class="w-full mx-auto">
        <Button @click="visible = true" label="Show Dialog" />
        <Dialog
          header="Edit Profile"
          v-model:visible="visible"
          content="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
        labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
        laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
        voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
        cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        />
      </div>
    </SectionLayout>
  </MainLayout>
</template>
