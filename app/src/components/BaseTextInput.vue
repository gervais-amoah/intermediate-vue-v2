<script setup lang="ts">
defineOptions({
  inheritAttrs: false,
})

defineProps({
  id: {
    type: String,
    required: true,
  },
  label: {
    type: String,
    required: true,
  },
})

const textValue = defineModel<string>()
</script>

<template>
  <div class="form-control">
    <label class="label" :for="id">
      <span class="label-text font-medium">{{ label }}</span>
    </label>
    <input
      :id="id"
      class="input input-bordered w-full"
      type="text"
      v-model="textValue"
      v-bind="$attrs"
    />
  </div>
</template>
