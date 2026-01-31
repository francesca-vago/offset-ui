<script setup lang="ts">
import SectionLayout from '../layouts/SectionLayout.vue'
import MainLayout from '../layouts/MainLayout.vue'
import Card from '../components/Card.vue'
</script>

<style scoped>
.color-card-blue {
  background-color: var(--color-offset-blue);
  padding-bottom: 8px;
}
.color-card-pink {
  background-color: var(--color-offset-pink);
  padding-bottom: 8px;
}
.color-card-green {
  background-color: var(--color-offset-green);
  padding-bottom: 8px;
}
.color-card-yellow {
  background-color: var(--color-offset-yellow);
  padding-bottom: 8px;
}
.color-card-red {
  background-color: var(--color-offset-red);
  padding-bottom: 8px;
}
.color-card-text {
  background-color: var(--color-text);
  padding-bottom: 8px;
}
.color-card-background {
  background-color: var(--color-background);
  padding-bottom: 8px;
}
.color-card-disabled {
  background-color: var(--color-disabled);
  padding-bottom: 8px;
}
</style>

<template>
  <MainLayout title="Overview">
    <SectionLayout title="Typography" class="flex flex-col gap-3">
      <h1>This is Heading 1</h1>
      <h2>This is Heading 2</h2>
      <h3>This is Heading 3</h3>
      <h4>This is Heading 4</h4>
      <h5>This is Heading 5</h5>
      <h6>This is Heading 6</h6>
      <p>This is a paragraph</p>
      <span>This is a span</span>
    </SectionLayout>

    <SectionLayout title="Colors">
      <div class="flex gap-3 mb-3">
        <Card
          title="Primary Blue"
          subtitle="#b8e2f2"
          class="bg-[var(--color-offset-blue)] pb-2"
          noFooter
        />
        <Card
          title="Primary Pink"
          subtitle="#f4bfd3"
          class="bg-[var(--color-offset-pink)] pb-2"
          noFooter
        />
        <Card
          title="Primary Purple"
          subtitle="#e3bff4"
          class="bg-[var(--color-offset-purple)] pb-2"
          noFooter
        />
      </div>
      <div class="flex gap-3 mb-3">
        <Card
          title="Success"
          subtitle="#ace8ca"
          class="bg-[var(--color-offset-green)] pb-2"
          noFooter
        />
        <Card
          title="Warning"
          subtitle="#f7eead"
          class="bg-[var(--color-offset-yellow)] pb-2"
          noFooter
        />
        <Card title="Error" subtitle="#f28183" class="bg-[var(--color-offset-red)] pb-2" noFooter />
      </div>
      <div class="flex gap-3 mb-3">
        <Card
          title="Text"
          subtitle="#0a0a0a"
          class="bg-[var(--color-text)] pb-2 text-white"
          noFooter
        />
        <Card
          title="Background"
          subtitle="#F5F5F5"
          class="bg-[var(--color-background)] pb-2"
          noFooter
        />
        <Card
          title="Disabled"
          subtitle="#E5E5E5"
          class="bg-[var(--color-disabled)] pb-2"
          noFooter
        />
      </div>
    </SectionLayout>

    <SectionLayout title="Spacing">
      <div class="w-10 h-10"></div>
    </SectionLayout>
  </MainLayout>
</template>
