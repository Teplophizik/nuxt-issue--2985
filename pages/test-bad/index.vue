<script setup>
const { data } = await useFetch(
  () => "https://6388772ca4bb27a7f7872d66.mockapi.io/test"
);
</script>

<template>
  <div>
    <p>Page test-bad</p>
    <NuxtPage :data="data" />
  </div>
</template>
