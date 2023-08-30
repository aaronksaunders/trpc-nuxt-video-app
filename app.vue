<script setup lang="ts">
const { $trpcClient } = useNuxtApp();
console.log($trpcClient);

const { data } = await $trpcClient.hello.useQuery({ text: "smith" });
</script>

<template>
  <p>app</p>
  <div>
    <p>{{ data?.greeting }}</p>
  </div>
</template>
