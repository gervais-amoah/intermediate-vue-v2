<script setup lang="ts">
import { ref } from 'vue'

const currentCount = ref(10)
</script>

<template>
  <div>
    <slot name="header">
      <h2>Slot Demo Title</h2>
    </slot>
    <slot :count="currentCount">
      <p>The count is {{ currentCount }}</p>
    </slot>
    <slot name="footer">
      <p>Default footer content</p>
    </slot>
  </div>
</template>

<style scoped></style>
