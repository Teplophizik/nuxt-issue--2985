<script setup>
const nestedShowed = ref(true);
const router = useRouter();
router.beforeEach((to, from) => {
  if (to.fullPath.split("/")[1] !== from.fullPath.split("/")[1]) {
    nestedShowed.value = false;
  }
});

const { data } = await useFetch(
  () => "https://6388772ca4bb27a7f7872d66.mockapi.io/test2"
);
</script>

<template>
  <div>
    <p>Page test-good2</p>
    <NuxtPage v-if="nestedShowed" :data2="data" />
  </div>
</template>
