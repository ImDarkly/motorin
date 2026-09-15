<script setup>
// TODO: defineProps for modelValue (Number)
const props = defineProps({
  modelValue: Number
})
// TODO: defineEmits for update:modelValue
const emit = defineEmits(['update:modelValue'])
</script>

<template>
  <div class="mileage-input">
    <!-- TODO: input type="number" step="0.1"
         Bind :value="modelValue"
         @input="emit('update:modelValue', $event.target.valueAsNumber)" -->
    <!-- TODO: span with "km" suffix -->
    <input type="number" step="0.1" :value="modelValue" @input="emit('update:modelValue', $event.target.valueAsNumber)" />
    <span>km</span>
  </div>
</template>

<style scoped>
.mileage-input {
  display: flex;
  align-items: center;
  gap: 4px;
}
.mileage-input input {
  width: 80px;
}
</style>
