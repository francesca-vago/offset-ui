<script setup lang="ts">
import Button from '../components/Button.vue'
import Input from '../components/Input.vue'
import Dialog from '../components/Dialog.vue'
import Card from '../components/Card.vue'
</script>

<template>
  <main>
    <h1>Components</h1>
    <h2>Buttons</h2>
    <Button label="Click me" />
    <Button label="Click me" icon="pi pi-check" />
    <h2>Inputs</h2>
    <Input placeholder="Enter your name" />
    <h2>Dialog</h2>
    <Dialog header="Edit Profile" />
    <h2>Card</h2>
    <Card header="Neo Brutalism" subtitle="Card Subtitle" />
  </main>
</template>
