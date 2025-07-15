<script setup lang="ts">
defineOptions({
  inheritAttrs: false,
})

defineProps({
  label: {
    type: String,
    required: true,
  },
  id: {
    type: String,
    required: true,
  },
  placeholder: {
    type: String,
    required: true,
  },
})

const textareaModel = defineModel<string>()
</script>

<template>
  <div class="form-control">
    <label class="label" :for="id">
      <span class="label-text font-medium">{{ label }}</span>
    </label>
    <textarea
      :id="id"
      class="textarea textarea-bordered w-full"
      rows="3"
      v-model="textareaModel"
      :placeholder="placeholder"
      v-bind="$attrs"
    ></textarea>
  </div>
</template>

<style scoped></style>
