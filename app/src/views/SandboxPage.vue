<script setup lang="ts">
import BaseTextarea from '@/components/BaseTextarea.vue'
import BaseTextInput from '@/components/BaseTextInput.vue'
import { ref } from 'vue'

const firstName = ref<string>('')
const lastName = ref<string>('')
const bio = ref<string>('')
</script>

<template>
  <div class="p-8 flex flex-col gap-4">
    <h1>Sandbox Page</h1>
    <p>This is a sandbox page for testing components and features.</p>
    <BaseTextInput
      id="test-input"
      label="User name"
      v-model:first-name="firstName"
      v-model:last-name="lastName"
    />
    <BaseTextarea id="bio-textarea" label="Bio" placeholder="Tell us about you..." v-model="bio" />
    <p>
      First name: <strong>{{ firstName }}</strong> <br />
      Last name: <strong>{{ lastName }}</strong> <br />
      Bio: <strong>{{ bio }}</strong>
    </p>
  </div>
</template>

<style scoped></style>
