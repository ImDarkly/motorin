<!--
Requirements — build PartsInventory.vue from scratch:
- Component uses reactive([...]) array of parts: { id, name, stock }
- Renders <ul> with v-for + :key="part.id"
- Each row: part name + <input type="number" v-model="part.stock"> + "units" label
- Button "Add Part" pushes { id: crypto.randomUUID(), name: 'New Part', stock: 0 }

Hints:
- reactive() wraps the array; v-for iterates it; :key binds to part.id for diffing.
- v-model on the input binds directly to part.stock (no .value needed in template).
- crypto.randomUUID() generates the new id; push mutates the reactive array in place.
-->

<script setup>
const parts = reactive([
  { id: 'p1', name: 'Brake Pads (front)', stock: 24 },
  { id: 'p2', name: 'Oil Filter', stock: 50 },
  { id: 'p3', name: 'Air Filter', stock: 18 },
  { id: 'p4', name: 'Spark Plugs (set of 4)', stock: 12 },
  { id: 'p5', name: 'Wiper Blades (pair)', stock: 30 },
]);
</script>

<template>
    <ul>
        <li v-for="part in parts" :key="part.id">
          <span>{{ part.name }}</span>
          <input type="number" v-model="part.stock" min="0" />
          <span>units</span>
        </li>
    </ul>
    <button @click="parts.push({ id: crypto.randomUUID(), name: 'New Part', stock: 0 })">Add Part</button>
</template>
