<script setup>
const props = defineProps(["data"]);

console.log("data", props.data);

const comp = computed(() =>
  props.data.map((el) => {
    const name = el.name + " - 1";
    return { id: el.id, name: name };
  })
);
</script>

<template>
  <p>Nested page test-good-index</p>
  <ul>
    <li v-for="d in comp" :key="d.id">{{ d.name }}</li>
  </ul>
</template>
