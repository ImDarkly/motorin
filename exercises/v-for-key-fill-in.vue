<script setup>
import { reactive } from 'vue'

const cars = reactive([
  { id: 'c1', make: 'Toyota', mileage: 42000 },
  { id: 'c2', make: 'Honda', mileage: 31000 },
  { id: 'c3', make: 'Ford', mileage: 58000 },
])
</script>

<template>
  <div class="car-list">
    <h2>Car Mileage Tracker</h2>
    <ul>
      <li
        v-for="car in cars" /* TODO: hint — v-for over cars */
        :key="car.id" /* TODO: hint — stable unique key, not index */
      >
        <label>
          {{ car.make }}
          <input
            type="number"
            v-model="car.mileage" /* TODO: hint — bind input to car.mileage */
          />
          miles
        </label>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.car-list { font-family: sans-serif; padding: 1rem; }
li { margin: 0.5rem 0; list-style: none; }
input { margin-left: 0.5rem; width: 6rem; }
</style>
