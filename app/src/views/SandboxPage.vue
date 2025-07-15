<script setup lang="ts">
import SlotDemo from '@/components/SlotDemo.vue'
import { ref } from 'vue'

const firstName = ref<string>('')
const lastName = ref<string>('')
const bio = ref<string>('')
</script>

<template>
  <main class="p-8 flex flex-col gap-4">
    <h1 class="text-2xl">Sandbox Page</h1>

    <SlotDemo>
      <template #header>
        <h2>Custom Header</h2>
      </template>

      <template #default="{ count }">
        <p>Current count is: {{ count }}</p>
      </template>

      <template #footer>
        <h2>Custom Footer</h2>
      </template>
    </SlotDemo>
  </main>
</template>

<style scoped></style>
