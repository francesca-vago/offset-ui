<script setup lang="ts">
import { RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
import { ref } from 'vue'

const items = ref([
  {
    label: 'Overview',
    icon: 'pi pi-home',
    route: '/',
  },
  {
    label: 'Alert',
    icon: 'pi pi-info-circle',
    route: '/alert',
  },
  {
    label: 'Buttons',
    icon: 'pi pi-info-circle',
    route: '/buttons',
  },
  {
    label: 'Card',
    icon: 'pi pi-info-circle',
    route: '/card',
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
    label: 'Menu',
    icon: 'pi pi-info-circle',
    route: '/menu',
  },
])
</script>

<template>
  <aside class="w-[250px] h-full p-4">
    <Menu :items>
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
  </aside>
  <main class="flex-1">
    <RouterView />
  </main>
</template>
