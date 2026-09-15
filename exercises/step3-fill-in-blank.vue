<script setup>
const props = defineProps(
['modelValue'] /* TODO: define the prop that v-model binds to by default */
)

const emit = defineEmits([
 'update:modelValue' /* TODO: define the event that v-model listens to by default */
])

function handleInput(newValue) {
 emit('update:modelValue', newValue) /* TODO: emit the update event with the new value */
}
</script>

<template>
  <div class="star-rating" role="radiogroup" aria-label="Rating">
    <span
      v-for="star in 5"
      :key="star"
      class="star"
      :class="{ filled: star <= props.modelValue }"
      @click="handleInput(star)"
    >
      ★
    </span>
  </div>
</template>

<style scoped>
.star-rating {
  display: flex;
  gap: 4px;
  font-size: 1.5rem;
  cursor: pointer;
}
.star {
  color: #ccc;
  transition: color 0.15s;
}
.star.filled {
  color: gold;
}
.star:hover {
  color: gold;
}
</style>
