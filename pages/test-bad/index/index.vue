<script setup>
const props = defineProps(["data"]);

console.log("data", props.data);
console.log("data", props.data[0].name);
</script>

<template>
  <p>Nested page test-bad-index</p>
  <ul>
    <li v-for="d in props.data" :key="d.id">{{ d.name }}</li>
  </ul>
</template>
