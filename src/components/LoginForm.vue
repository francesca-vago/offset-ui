<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { cn } from '@/lib/utils'
import Button from '@/components/Button.vue'
import { Card, CardContent, CardDescription, CardHeader, CardTitle } from '@/components/Card'
import InputText from '@/components/Input.vue'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()
</script>

<template>
  <div :class="cn('flex flex-col gap-6', props.class)">
    <Card>
      <CardHeader>
        <CardTitle>Login to your account</CardTitle>
        <CardDescription> Enter your email below to login to your account </CardDescription>
      </CardHeader>
      <CardContent>
        <form>
          <label for="email"> Email </label>
          <InputText id="email" type="email" placeholder="m@example.com" required />
          <div class="flex items-center">
            <label for="password"> Password </label>
            <a href="#" class="ml-auto inline-block text-sm underline-offset-4 hover:underline">
              Forgot your password?
            </a>
          </div>
          <InputText id="password" type="password" required />
          <Button type="submit"> Login </Button>
          <Button variant="outline" type="button"> Login with Google </Button>
        </form>
      </CardContent>
    </Card>
  </div>
</template>
