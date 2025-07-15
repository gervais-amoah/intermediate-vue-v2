<script setup lang="ts">
import BaseTExtInput from '@/components/BaseTExtInput.vue'
import { ref } from 'vue'

const firstName = ref<string>('')
const lastName = ref<string>('')
</script>

<template>
  <h1>Sandbox Page</h1>
  <p>This is a sandbox page for testing components and features.</p>
  <BaseTExtInput
    id="test-input"
    label="User name"
    v-model:first-name="firstName"
    v-model:last-name="lastName"
  />
  <p>
    First name: <strong>{{ firstName }}</strong> Last name: <strong>{{ lastName }}</strong>
  </p>
</template>

<style scoped></style>
