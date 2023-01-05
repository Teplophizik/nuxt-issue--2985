<script setup>
const { data } = await useFetch(
  () => "https://6388772ca4bb27a7f7872d66.mockapi.io/test2"
);
</script>

<template>
  <div>
    <p>Page test-bad2</p>
    <NuxtPage :data2="data" />
  </div>
</template>
