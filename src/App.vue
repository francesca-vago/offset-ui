<script setup lang="ts">
import { RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
import { ref } from 'vue'

const items = ref([
  {
    label: 'Overview',
    route: '/',
  },
  {
    label: 'Alert',
    route: '/alert',
  },
  {
    label: 'Buttons',
    route: '/buttons',
  },
  {
    label: 'Card',
    route: '/card',
  },
  {
    label: 'Dialog',
    route: '/dialog',
  },
  {
    label: 'Inputs',
    route: '/inputs',
  },
  {
    label: 'Menu',
    route: '/menu',
  },
])
</script>

<template>
  <aside class="w-[250px] h-full p-4">
    <Menu :items>
      <template #item="{ item, props }">
        <router-link v-if="item.route" v-slot="{ href, navigate }" :to="item.route" custom>
          <a
            v-ripple
            :href="href"
            v-bind="props.action"
            @click="navigate"
            class="block w-full hover:bg-[var(--color-neutral-100)]"
          >
            <span v-if="item.icon" :class="item.icon" />
            <span class="ml-2">{{ item.label }}</span>
          </a>
        </router-link>
        <a
          v-else
          v-ripple
          :href="item.url"
          :target="item.target"
          v-bind="props.action"
          class="block w-full hover:bg-[var(--color-neutral-100)]"
        >
          <span v-if="item.icon" :class="item.icon" />
          <span class="ml-2">{{ item.label }}</span>
        </a>
      </template>
    </Menu>
  </aside>
  <main class="flex-1">
    <RouterView />
  </main>
</template>
