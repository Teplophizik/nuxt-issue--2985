<script setup>
const props = defineProps(["data2"]);

console.log("data2", props.data2);
console.log("data2", props.data2[0].name);
</script>

<template>
  <p>Nested page test-good2-index</p>
  <ul>
    <li v-for="d in props.data2" :key="d.id">{{ d.name }}</li>
  </ul>
</template>
