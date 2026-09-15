<script setup>
const props = defineProps({
  modelValue: Boolean
})

const emit = defineEmits([
  'update:modelValue'
])

function toggle() {
  emit('update:modelValue', !props.modelValue)
}
</script>

<template>
  <button @click="toggle" :class="{ active: props.modelValue }">
    {{ props.modelValue ? '★ Favorited' : '☆ Add favorite' }}
  </button>
</template>

<style scoped>
.active { color: gold; }
</style>