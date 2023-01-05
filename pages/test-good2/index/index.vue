<script setup>
const props = defineProps(["data2"]);

console.log("data2", props.data2);

const comp = computed(() =>
  props.data2.map((el) => {
    const name = el.name + " - 2";
    return { id: el.id, name: name };
  })
);
</script>

<template>
  <p>Nested page test-good2-index</p>
  <ul>
    <li v-for="d in comp" :key="d.id">{{ d.name }}</li>
  </ul>
</template>
