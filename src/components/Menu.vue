<script setup lang="ts">
import Menu from 'primevue/menu'
import { ref } from 'vue'

const items = ref([
  {
    label: 'Home',
    icon: 'pi pi-home',
    route: '/',
  },
  {
    label: 'Buttons',
    icon: 'pi pi-info-circle',
    route: '/buttons',
  },
  {
    label: 'Inputs',
    icon: 'pi pi-info-circle',
    route: '/inputs',
  },
  {
    label: 'Dialog',
    icon: 'pi pi-info-circle',
    route: '/dialog',
  },
  {
    label: 'Card',
    icon: 'pi pi-info-circle',
    route: '/card',
  },
])
</script>

<template>
  <Menu :model="items">
    <template #item="{ item, props }">
      <router-link v-if="item.route" v-slot="{ href, navigate }" :to="item.route" custom>
        <a v-ripple :href="href" v-bind="props.action" @click="navigate">
          <span :class="item.icon" />
          <span class="ml-2">{{ item.label }}</span>
        </a>
      </router-link>
      <a v-else v-ripple :href="item.url" :target="item.target" v-bind="props.action">
        <span :class="item.icon" />
        <span class="ml-2">{{ item.label }}</span>
      </a>
    </template>
  </Menu>
</template>
