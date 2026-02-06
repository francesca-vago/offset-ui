<script setup lang="ts">
import {
  Card,
  CardTitle,
  CardDescription,
  CardContent,
  CardAction,
  CardHeader,
} from '@/components/Card'
import SectionLayout from '@/layouts/SectionLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
import Button from '@/components/Button.vue'
</script>

<template>
  <MainLayout title="Cards">
    <SectionLayout title="Card with Image">
      <div class="w-80 mx-auto">
        <Card
          class="shadow-[4px_4px_0_0_#000000] border-black rounded-sm border-2 overflow-hidden w-full max-w-2xl h-fit"
        >
          <CardHeader>
            <div class="w-full h-full">
              <img
                class="w-full h-full object-cover"
                alt="Image Description"
                src="@/images/lemon-illustration.jpg"
              />
            </div>
          </CardHeader>
          <CardTitle>
            <h4 class="px-5 pt-5">Neo Brutalism</h4>
          </CardTitle>
          <CardDescription>
            <span class="px-5 text-neutral-500 font-medium">31/01/2026</span>
          </CardDescription>
          <CardContent>
            <p class="mt-1 text-xs! text-justify text-wrap">
              Neobrutalism is an aesthetic characterized by high contrast elements, bright colors,
              and bold shapes. It is often used to make a statement, as it is meant to be
              eye-catching and stand out to the viewer.
            </p>
          </CardContent>
          <CardAction class="flex justify-end gap-2 px-5 py-5">
            <Button label="Read More" size="sm" variant="text" />
          </CardAction>
        </Card>
      </div>
    </SectionLayout>
    <SectionLayout title="Card without Image">
      <div class="w-80 mx-auto">
        <Card>
          <CardTitle>
            <h4 class="px-5 pt-5">Neo Brutalism</h4>
          </CardTitle>
          <CardDescription>
            <span class="px-5 text-neutral-500 font-medium">31/01/2026</span>
          </CardDescription>
          <CardContent>
            <p class="px-5 mt-1 text-xs! text-justify text-wrap">
              Neobrutalism is an aesthetic characterized by high contrast elements, bright colors,
              and bold shapes. It is often used to make a statement, as it is meant to be
              eye-catching and stand out to the viewer.
            </p>
          </CardContent>
          <CardAction>
            <Button label="Read More" size="sm" variant="text" />
          </CardAction>
        </Card>
      </div>
    </SectionLayout>
  </MainLayout>
</template>
