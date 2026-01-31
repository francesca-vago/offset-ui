<script setup lang="ts">
import { RouterView } from 'vue-router'
import Menu from './components/Menu.vue'
import Navbar from './components/Navbar.vue'
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
  <Navbar />
  <div class="flex">
    <aside class="h-full min-w-[250px]">
      <Menu :items>
        <template #item="{ item, props }">
          <router-link
            v-if="item.route"
            v-slot="{ href, navigate, isActive }"
            :to="item.route"
            custom
          >
            <a
              v-ripple
              :href="href"
              v-bind="props.action"
              @click="navigate"
              class="block w-auto text-lg font-semibold hover:bg-[var(--color-offset-purple)] border-2 hover:border-black m-2"
              :class="[
                isActive ? 'border-black bg-[var(--color-offset-purple)]' : 'border-transparent',
              ]"
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
            class="block w-full"
          >
            <span v-if="item.icon" :class="item.icon" />
            <span class="ml-2">{{ item.label }}</span>
          </a>
        </template>
      </Menu>
    </aside>
    <div class="flex-1 h-dvh flex flex-col">
      <RouterView />
    </div>
  </div>
</template>
