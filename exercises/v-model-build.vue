<script setup></script>

<template></template>

<!-- Requirements: MileageInput.vue
     - Component name: MileageInput.vue
     - Accepts v-model (number, kilometers)
     - Renders <input type="number"> with step="0.1"
     - Shows "km" suffix label
     - Emits update on input event (not change)
     - No other props, no extra features
-->

<!-- Hints:
     1. defineProps({ modelValue: Number }) + defineEmits(['update:modelValue'])
     2. Bind :value="modelValue" and @input="emit('update:modelValue', $event.target.valueAsNumber)"
     3. Use input event (not change) so updates fire on every keystroke
-->

<!-- Why would you emit on input rather than change here? What breaks if you
     use change for a mileage tracker that needs live updates? -->
