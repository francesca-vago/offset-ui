<script setup lang="ts">
import Input from '@/components/Input.vue'
import TextArea from '@/components/TextArea.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
import Switch from '@/components/ToggleSwitch.vue'
import Checkbox from '@/components/Checkbox.vue'

import { ref } from 'vue'

const checked = ref(true)
</script>

<template>
  <MainLayout title="Inputs">
    <SectionLayout title="Input Text">
      <Input placeholder="Enter your name" />
    </SectionLayout>
    <SectionLayout title="Textarea">
      <TextArea placeholder="Enter your message" />
    </SectionLayout>
    <SectionLayout title="Checkbox">
      <Checkbox
        v-model:checked="checked"
        label="Checkbox"
        input-id="checkbox"
        name="checkbox"
        value="checkbox"
      />
    </SectionLayout>
    <SectionLayout title="Switch">
      <Switch />
    </SectionLayout>
  </MainLayout>
</template>
