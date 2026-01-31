<script setup lang="ts">
import Menu from '@/components/Menu.vue'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
import { ref } from 'vue'

const items = ref([
  {
    label: 'Settings',
    icon: 'pi pi-home',
  },
  {
    label: 'Messages',
    icon: 'pi pi-home',
  },
  {
    label: 'Logout',
    icon: 'pi pi-home',
  },
])
</script>

<template>
  <MainLayout title="Menu">
    <SectionLayout title="Menu List">
      <div class="border border-black md:w-80">
        <Menu :items="items">
          <template #item="{ item, props }">
            <router-link v-if="item.route" v-slot="{ href, navigate }" :to="item.route" custom>
              <a v-ripple :href="href" v-bind="props.action" @click="navigate">
                <span v-if="item.icon" :class="item.icon" />
                <span class="ml-2">{{ item.label }}</span>
              </a>
            </router-link>
            <a v-else v-ripple :href="item.url" :target="item.target" v-bind="props.action">
              <span v-if="item.icon" :class="item.icon" />
              <span class="ml-2">{{ item.label }}</span>
            </a>
          </template>
        </Menu>
      </div>
    </SectionLayout>
  </MainLayout>
</template>
