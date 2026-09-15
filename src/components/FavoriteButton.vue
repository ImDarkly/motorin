<template>
  <button @click="toggle">
    {{ isFav ? '★ Favorited' : '☆ Add favorite' }}
  </button>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  modelValue: Boolean
});

const emit = defineEmits(['update:modelValue']);

const isFav = computed(() => props.modelValue);

function toggle() {
  /* TODO: emit the new boolean value so the parent updates */
  emit(/* TODO: event name and new value */);
}
</script>
